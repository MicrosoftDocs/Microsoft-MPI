---
title: MPI_Iallreduce function
TOCTitle: MPI_Iallreduce function
ms:assetid: 0E94E7ED-8194-4AFE-B287-765914559DEA
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Mt629167(v=VS.85)
ms:contentKeyID: 71965703
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ALLREDUCE
- mpi/MPI_ALLREDUCE
- mpif/MPI_ALLREDUCE
- mpi/MPI_Iallreduce
- MPI_Iallreduce
- mpif/MPI_Iallreduce
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Iallreduce
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn about the MPI_Iallreduce function on Microsoft's platform. This article provides a detailed explanation of parameters, syntax, and usage for efficient data processing.
---

# MPI\_Iallreduce function

Combines values from all processes and distributes the result back to all processes in a non-blocking way.

## Syntax

``` c++
int MPIAPI MPI_Iallreduce(
  _In_opt_  const void         *sendbuf,
  _Out_opt_       void         *recvbuf,
  _In_            int          count,
  _In_            MPI_Datatype datatype,
  _In_            MPI_Op       op,
  _In_            MPI_Comm     comm,
  _Out_           MPI_Request  *request
);
```

## Parameters

  - *sendbuf* \[in, optional\]  
    The pointer to the data to be sent to all processes in the group. The number and data type of the elements in the buffer are specified in the *count* and *datatype* parameters.
    
    If the *comm* parameter references an intracommunicator, you can specify an in-place option by specifying **MPI\_IN\_PLACE** in all processes. In this case, the input data is taken at each process from the receive buffer, where it will be replaced by the output data.

  - *recvbuf* \[out, optional\]  
    The pointer to a buffer to receive the result of the reduction operation.

  - *count* \[in\]  
    The number of elements to send from this process.

  - *datatype* \[in\]  
    The data type of each element in the buffer. This parameter must be compatible with the operation as specified in the *op* parameter.

  - *op* \[in\]  
    The global reduction operation to perform. The handle can indicate a built-in or application-defined operation. For a list of predefined operations, see [**MPI\_Op**](mpi-op-enumeration.md).

  - *comm* \[in\]  
    The [**MPI\_Comm**](mpi-comm-enumeration.md) communicator handle.

  - *request* \[out\]  
    The [**MPI\_Request**](mpi-comm-enumeration.md) handle representing the communication operation.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_IALLREDUCE(SENDBUF, RECVBUF, COUNT, DATATYPE, OP, COMM, REQUEST, IERROR)
        <type> SENDBUF(*), RECVBUF(*)
        INTEGER COUNT, DATATYPE, OP, COMM, REQUEST, IERROR
```

## Remarks

A non-blocking call initiates a collective reduction operation which must be completed in a separate completion call. Once initiated, the operation may progress independently of any computation or other communication at participating processes. In this manner, non-blocking reduction operations can mitigate possible synchronizing eﬀects of reduction operations by running them in the “background.”

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
<td><p>Microsoft MPI v7</p></td>
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

[**MPI\_Datatype**](mpi-datatype-enumeration.md)

[**MPI\_Op**](mpi-op-enumeration.md)

[**MPI\_Allreduce**](mpi-allreduce-function.md)

[**MPI\_Test**](mpi-test-function.md)

[**MPI\_Testall**](mpi-testall-function.md)

[**MPI\_Testany**](mpi-testany-function.md)

[**MPI\_Testsome**](mpi-testsome-function.md)

[**MPI\_Wait**](mpi-wait-function.md)

[**MPI\_Waitall**](mpi-waitall-function.md)

[**MPI\_Waitany**](mpi-waitany-function.md)

[**MPI\_Waitsome**](mpi-waitsome-function.md)

