---
title: MPI_Igather function
TOCTitle: MPI_Igather function
ms:assetid: 60C7DA65-D001-4959-AE7C-78D943A981EA
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Mt131842(v=VS.85)
ms:contentKeyID: 65834028
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_IGATHER
- mpif/MPI_Igather
- mpi/MPI_IGATHER
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Igather
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn how to use the MPI_Igather function for non-blocking data gathering in Microsoft MPI. Detailed syntax, parameters, and return values explained.
---

# MPI\_Igather function

Gathers data from all members of a group to one member in a non-blocking way.

## Syntax

``` c++
int WINAPI MPI_Igather(
  _In_      void         *sendbuf,
            int          sendcount,
            MPI_Datatype sendtype,
  _Out_opt_ void         *recvbuf,
  _In_      int          recvcount,
  _In_      MPI_Datatype recvtype,
  _In_      int          root,
  _In_      MPI_Comm     comm,
  _Out_     MPI_Request  *request
);
```

## Parameters

  - *sendbuf* \[in\]  
    The pointer to a buffer containing the data to be sent to the root. The buffer consists of *sendcount* successive elements of the **MPI\_Datatype** indicated by the *sendtype* handle. The message length is specified in terms of number of elements, not number of bytes.

  - *sendcount*  
    The number of *sendtype* elements in *sendbuf*. If the value is zero, the data part of the message is empty.

  - *sendtype*  
    The **MPI\_Datatype** handle representing the data type of each element in *sendbuf*.

  - *recvbuf* \[out, optional\]  
    The pointer to a buffer containing the data received from each process on the root, including data sent by the root process (significant only at root). The receive buffer *recvbuf* is ignored for all non-root processes. On the root process, *recvbuf* consists of *recvcount* successive elements of the **MPI\_Datatype** indicated by the *recvtype* handle. The message length is specified in terms of number of elements, not number of bytes.

  - *recvcount* \[in\]  
    The number of *recvtype* elements in *recvbuf*. If the value is zero, the data part of the message is empty (significant only at root).

  - *recvtype* \[in\]  
    The **MPI\_Datatype** handle representing the data type of each element in *recvbuf* (significant only at root).

  - *root* \[in\]  
    The rank of the receiving process within the [**MPI\_Comm**](mpi-comm-enumeration.md)*comm.*

  - *comm* \[in\]  
    The [**MPI\_Comm**](mpi-comm-enumeration.md) communicator handle.

  - *request* \[out\]  
    The **MPI\_Request** handle representing the communication operation.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_IGATHER(SENDBUF, SENDCOUNT, SENDTYPE, RECVBUF, RECVCOUNT, RECVTYPE,
    ROOT, COMM, REQUEST, IERROR)
        <type> SENDBUF(*), RECVBUF(*)
        INTEGER SENDCOUNT, SENDTYPE, RECVCOUNT, RECVTYPE, ROOT, COMM, REQUEST, IERROR
```

## Remarks

A non-blocking call initiates a collective gather operation which must be completed in a separate completion call. Once initiated, the operation may progress independently of any computation or other communication at participating processes. In this manner, non-blocking gather operations can mitigate possible synchronizing eﬀects of gather operations by running them in the “background.”

All completion calls (e.g., [**MPI\_Wait**](mpi-wait-function.md)) are supported for non-blocking gather operations.

## Requirements

<table>
<colgroup>
<col/>
<col/>
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

[**MPI\_Gather**](mpi-gatherv-function.md)

[**MPI\_Test**](mpi-test-function.md)

[**MPI\_Testall**](mpi-testall-function.md)

[**MPI\_Testany**](mpi-testany-function.md)

[**MPI\_Testsome**](mpi-testsome-function.md)

[**MPI\_Wait**](mpi-wait-function.md)

[**MPI\_Waitall**](mpi-waitall-function.md)

[**MPI\_Waitany**](mpi-waitany-function.md)

[**MPI\_Waitsome**](mpi-waitsome-function.md)

