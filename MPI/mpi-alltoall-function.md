---
title: MPI_Alltoall function
TOCTitle: MPI_Alltoall function
ms:assetid: 1fde8800-421a-45d3-ba4d-be0237003b61
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473230(v=VS.85)
ms:contentKeyID: 59360776
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ALLTOALL
- mpif/MPI_Alltoall
- mpi/MPI_ALLTOALL
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Alltoall
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Master the MPI_Alltoall Function: gather & scatter data efficiently with Microsoft's Message Passing Interface. Learn syntax, parameters & more.
---

# MPI\_Alltoall function

Gathers data from and scatters data to all members of a group. The **MPI\_Alltoall** is an extension of the [**MPI\_Allgather**](mpi-allgather-function.md) function. Each process sends distinct data to each of the receivers. The *j*th block that is sent from process *i* is received by process *j* and is placed in the *i*th block of the receive buffer.

## Syntax

``` c++
int MPIAPI MPI_Alltoall(
  _In_  void         *sendbuf,
        int          sendcount,
        MPI_Datatype sendtype,
  _Out_ void         *recvbuf,
        int          recvcount,
        MPI_Datatype recvtype,
        MPI_Comm     comm
);
```

## Parameters

  - *sendbuf* \[in\]  
    The pointer to the data to be sent to all processes in the group. The number and data type of the elements in the buffer are specified in the *sendcount* and *sendtype* parameters.
    
    If the comm parameter references an intracommunicator, you can specify an in-place option by specifying **MPI\_IN\_PLACE** in all processes. The *sendcount* and *sendtype* parameters are ignored. Each process enters data in the corresponding receive buffer element. The *n*th process sends data to the *n*th element of the receive buffer.

  - *sendcount*  
    The number of elements in the buffer that is specified in the *sendbuf* parameter. If *sendcount* is zero, the data part of the message is empty.

  - *sendtype*  
    The MPI data type of the elements in the send buffer.

  - *recvbuf* \[out\]  
    The pointer to a buffer that contains the data that is received from each process. The number and data type of the elements in the buffer are specified in the *recvcount* and *recvtype* parameters.

  - *recvcount*  
    The number of elements in the receive buffer. If the count is zero, the data part of the message is empty.

  - *recvtype*  
    The MPI data type of the elements in the receive buffer.

  - *comm*  
    The [**MPI\_Comm**](mpi-comm-enumeration.md) communicator handle.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_ALLTOALL(SENDBUF, SENDCOUNT, SENDTYPE, RECVBUF, RECVCOUNT, RECVTYPE,
                COMM, IERROR)
        <type> SENDBUF(*), R.ECVBUF(*)
        INTEGER SENDCOUNT, SENDTYPE, RECVCOUNT, RECVTYPE, COMM, IERROR
```

## Remarks

All parameters are significant on all processes. The *comm* parameter must be identical on all processes.

The type signature that is specified by the *sendcount*, and *sendtype* parameters for a process must be equal to the type signature that is specified by the *recvcount*, and *recvtype* parameters. Therefore, the amount of data sent must be equal to the amount of data that is received between any pair of processes. Distinct type maps between sender and receiver are still allowed.

If the *comm* parameter references an intracommunicator, the outcome of a call to `MPI_ALLGATHER(...)` is as if each process executed a send to each process including itself by using `MPI_Send(sendbuf + i*sendcount*extent(sendtype), sendcount, sendtype, I, …)`, and receiving from every other process by using `MPI_Recv(recvbuf + i*recvcount*extent(recvtype), recvcount, recvtype, I, …)`.

If the *comm* parameter references an intercommunicator, then the result is as if each process in group A sends a message to each process in group B, and vice versa. The *j*th send buffer of process *i* in group A should be consistent with the *i*th receive buffer of process *j* in group B, and vice versa.

The number of items that is sent by processes in group A, do not have to be equal the number of items that is sent by processes in group B. In particular, you can move data in only one direction by specifying *sendcount* == 0 for the communication in the reverse direction.

## Requirements

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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

[**MPI\_Datatype**](mpi-datatype-enumeration.md)

[**MPI\_Allgather**](mpi-allgather-function.md)

[**MPI\_Send**](mpi-send-function.md)

[**MPI\_Recv**](mpi-recv-function.md)

