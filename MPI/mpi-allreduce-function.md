---
title: MPI_Allreduce function
TOCTitle: MPI_Allreduce function
ms:assetid: 4ff26760-0a3f-4927-8c8d-ac7d7f662039
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn502503(v=VS.85)
ms:contentKeyID: 59360775
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ALLREDUCE
- mpif/MPI_Allreduce
- mpi/MPI_ALLREDUCE
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Allreduce
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Explore the MPI_Allreduce function on Microsoft's learning platform. Understand its syntax, parameters, return values, and how it combines values from all processes.
---

# MPI\_Allreduce function

Combines values from all processes and distributes the result back to all processes.

## Syntax

``` c++
int MPIAPI MPI_Allreduce(
  _In_opt_  const void         *sendbuf,
  _Out_opt_       void         *recvbuf,
  _In_            int          count,
  _In_            MPI_Datatype datatype,
  _In_            MPI_Op       op,
  _In_            MPI_Comm     comm
);
```

## Parameters

  - *sendbuf* \[in, optional\]  
    The pointer to the data to be sent to all processes in the group. The number and data type of the elements in the buffer are specified in the count and datatype parameters.
    
    If the *comm* parameter references an intracommunicator, you can specify an in place option by specifying **MPI\_IN\_PLACE** in all processes. In this case, the input data is taken at each process from the receive buffer, where it will be replaced by the output data.

  - *recvbuf* \[out, optional\]  
    The pointer to a buffer to receive the result of the reduction operation. This parameter is significant only at the root process.

  - *count* \[in\]  
    The number of elements to send from this process.

  - *datatype* \[in\]  
    The **MPI\_Datatype** of each element in the buffer. This parameter must be compatible with the operation as specified in the *op* parameter.

  - *op* \[in\]  
    The **MPI\_Op** handle indicating the global reduction operation to perform. The handle can indicate a built-in or application-defined operation. For a list of predefined operations, see [**MPI\_Op**](mpi-op-enumeration.md).

  - *comm* \[in\]  
    The [**MPI\_Comm**](mpi-comm-enumeration.md) communicator handle.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_ALLREDUCE(SENDBUF, RECVBUF, COUNT, DATATYPE, OP, COMM, IERROR)
        <type> SENDBUF(*), RECVBUF(*)
        INTEGER COUNT, DATATYPE, OP, COMM, IERROR
```

## Remarks

If *comm* is an intercommunicator, the result of the reduction of the data provided by processes in group A is stored at each process in group B, and vice versa. Both groups should provide *count* and *datatype* arguments that specify the same type signature.

All completion calls (e.g., [**MPI\_Wait**](mpi-wait-function.md)) are supported for non-blocking reduction operations.

## Requirements

<table>
<colgroup>
<col/>
<col/>
</colgroup>
<tbody>
<tr class="odd">
<td><p>Product</p></td>
<td><p>HPC Pack 2012 MS-MPI Redistributable Package, HPC Pack 2008 R2 MS-MPI Redistributable Package, HPC Pack 2008 MS-MPI Redistributable Package or HPC Pack 2008 Client Utilities</p></td>
</tr>
<tr class="even">
<td><p>Header</p></td>
<td>Mpi.h;
Mpif.h</td>
</tr>
<tr class="odd">
<td><p>Library</p></td>
<td>Msmpi.lib</td>
</tr>
<tr class="even">
<td><p>DLL</p></td>
<td>Msmpi.dll</td>
</tr>
</tbody>
</table>


## See also

[MPI Collective Functions](mpi-collective-functions.md)

[**MPI\_Reduce**](mpi-reduce-function.md)

[**MPI\_Datatype**](mpi-datatype-enumeration.md)

[**MPI\_Op**](mpi-op-enumeration.md)

