---
title: MPI_Ireduce function
TOCTitle: MPI_Ireduce function
ms:assetid: 8EE81913-0713-4FF3-8723-0EC6641583E3
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn985831(v=VS.85)
ms:contentKeyID: 65288035
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_IREDUCE
- mpif/MPI_Ireduce
- mpi/MPI_IREDUCE
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Ireduce
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
---

# MPI\_Ireduce function

Performs a global reduce operation (for example sum, maximum, or logical and) across all members of a group in a non-blocking way.

## Syntax

``` c++
int MPIAPI MPI_Ireduce(
  _In_      void         *sendbuf,
  _Out_opt_ void         *recvbuf,
  _In_      int          count,
  _In_      MPI_Datatype datatype,
  _In_      MPI_Op       op,
  _In_      int          root,
  _In_      MPI_Comm     comm,
  _Out_     MPI_Request  *request
);
```

## Parameters

  - *sendbuf* \[in\]  
    The pointer to a buffer containing the data from this rank to be used in the reduction. The buffer consists of *count* successive elements of the **MPI\_Datatype** indicated by the *datatype* handle. The message length is specified in terms of number of elements, not number of bytes.

  - *recvbuf* \[out, optional\]  
    The pointer to a buffer to receive the result of the reduction operation. This parameter is significant only at the root process.

  - *count* \[in\]  
    The number of elements to send from this process.

  - *datatype* \[in\]  
    The **MPI\_Datatype** handle representing the data type of each element in *sendbuf*.

  - *op* \[in\]  
    The **MPI\_Op** handle indicating the global reduction operation to perform. The handle can indicate a built-in or application defined operation. For a list of predefined operations, see the [**MPI\_Op**](mpi-op-enumeration.md) topic.

  - *root* \[in\]  
    The rank of the receiving process within the [**MPI\_Comm**](mpi-comm-enumeration.md) *comm*.

  - *comm* \[in\]  
    The [**MPI\_Comm**](mpi-comm-enumeration.md) communicator handle.

  - *request* \[out\]  
    The **MPI\_Request** handle representing the communication operation..

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_IREDUCE(SENDBUF, RECVBUF, COUNT, DATATYPE, OP, ROOT, COMM, REQUEST, IERROR) 
        <type> SENDBUF(*), RECVBUF(*) 
        INTEGER COUNT, DATATYPE, OP, ROOT, COMM, REQUEST, IERROR

## Remarks

A non-blocking call initiates a collective reduction operation which must be completed in a separate completion call. Once initiated, the operation may progress independently of any computation or other communication at participating processes. In this manner, non-blocking reduction operations can mitigate possible synchronizing eﬀects of reduction operations by running them in the “background.”

All completion calls (e.g., [**MPI\_Wait**](mpi-wait-function.md)) are supported for non-blocking reduction operations.

## Requirements

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Product</p></td>
<td><p>Microsoft MPI v6</p></td>
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

[**MPI\_Reduce**](mpi-reduce-function.md)

[**MPI\_Test**](mpi-test-function.md)

[**MPI\_Testall**](mpi-testall-function.md)

[**MPI\_Testany**](mpi-testany-function.md)

[**MPI\_Testsome**](mpi-testsome-function.md)

[**MPI\_Wait**](mpi-wait-function.md)

[**MPI\_Waitall**](mpi-waitall-function.md)

[**MPI\_Waitany**](mpi-waitany-function.md)

[**MPI\_Waitsome**](mpi-waitsome-function.md)

