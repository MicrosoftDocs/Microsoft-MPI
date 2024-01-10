---
title: MPI_Iallgather function
TOCTitle: MPI_Iallgather function
ms:assetid: E4849DDC-80B0-4AB8-83E7-F7FB0A21A89B
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Mt629166(v=VS.85)
ms:contentKeyID: 71965702
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_IALLGATHER
- mpif/MPI_Iallgather
- mpi/MPI_IALLGATHER
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_IAllgather
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn about the MPI_Iallgather function on Microsoft's platform. This article provides a detailed explanation of its syntax, parameters, and usage.
---

# MPI\_Iallgather function

Gathers data from all members of a group and sends the data to all members of the group in a non-blocking way.

## Syntax

``` c++
int MPIAPI MPI_Iallgather(
  _In_opt_  const void         *sendbuf,
  _In_             int         sendcount,
  _In_            MPI_Datatype sendtype,
  _Out_opt_       void         *recvbuf,
  _In_            int          recvcount,
  _In_            MPI_Datatype recvtype,
  _In_            MPI_Comm     comm,
  _Out_           MPI_Request  *request
);
```

## Parameters

  - *sendbuf* \[in, optional\]  
    The pointer to the data to be sent to all processes in the group. The number and data type of the elements in the buffer are specified in the *sendcount* and *sendtype* parameters. Each element in the buffer corresponds to a process in the group.
    
    If the comm parameter references an intracommunicator, you can specify an in-place option by specifying **MPI\_IN\_PLACE** in all processes. The *sendcount* and *sendtype* parameters are ignored. Each process enters data in the corresponding receive buffer element. The *n*th process sends data to the *n*th element of the receive buffer.

  - *sendcount* \[in\]  
    The number of elements in the buffer that is specified in the *sendbuf* parameter. If *sendcount* is zero, the data part of the message is empty.

  - *sendtype* \[in\]  
    The MPI data type of the elements in the send buffer.

  - *recvbuf* \[out, optional\]  
    The pointer to a buffer that contains the data that is received from each process. The number and data type of the elements in the buffer are specified in the *recvcount* and *recvtype* parameters.

  - *recvcount* \[in\]  
    The number of elements in the receive buffer. If the count is zero, the data part of the message is empty.

  - *recvtype* \[in\]  
    The MPI data type of the elements in the receive buffer.

  - *comm* \[in\]  
    The [**MPI\_Comm**](mpi-comm-enumeration.md) communicator handle.

  - *request* \[out\]  
    The [**MPI\_Request**](mpi-comm-enumeration.md) handle representing the communication operation.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_IALLGATHER(SENDBUF, SENDCOUNT, SENDTYPE, RECVBUF, RECVCOUNT, RECVTYPE, COMM, REQUEST, IERROR)
        <type> SENDBUF(*), RECVBUF(*)
        INTEGER SENDCOUNT, SENDTYPE, RECVCOUNT, RECVTYPE, COMM, REQUEST, IERROR
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

[**MPI\_Gather**](mpi-gather-function.md)

[**MPI\_Datatype**](mpi-datatype-enumeration.md)

[**MPI\_Test**](mpi-test-function.md)

[**MPI\_Testall**](mpi-testall-function.md)

[**MPI\_Testany**](mpi-testany-function.md)

[**MPI\_Testsome**](mpi-testsome-function.md)

[**MPI\_Wait**](mpi-wait-function.md)

[**MPI\_Waitall**](mpi-waitall-function.md)

[**MPI\_Waitany**](mpi-waitany-function.md)

[**MPI\_Waitsome**](mpi-waitsome-function.md)

