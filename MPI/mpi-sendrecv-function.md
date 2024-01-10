---
title: MPI_Sendrecv function
TOCTitle: MPI_Sendrecv function
ms:assetid: a79b2c21-bbab-4aeb-b612-8f11796d1512
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473468(v=VS.85)
ms:contentKeyID: 59361003
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_SENDRECV
- mpif/MPI_Sendrecv
- mpi/MPI_SENDRECV
dev_langs:
- C++
- C
description: "Master the MPI_Sendrecv Function: Efficient Message Passing Interface for Microsoft HPC Pack. Learn syntax, parameters & more."
---

# MPI\_Sendrecv function

Sends and receives a message.

## Syntax

``` c++
int MPIAPI MPI_Sendrecv(
  _In_  void         *sendbuf,
        int          sendcount,
        MPI_Datatype sendtype,
        int          dest,
        int          sendtag,
  _Out_ void         *recvbuf,
        int          recvcount,
        MPI_Datatype recvtype,
        int          source,
        int          recvtag,
        MPI_Comm     comm,
  _Out_ MPI_Status   *status
);
```

## Parameters

  - *sendbuf* \[in\]  
    Initial address of send buffer.

  - *sendcount*  
    Number of elements in send buffer.

  - *sendtype*  
    Type of elements in send buffer.

  - *dest*  
    Rank of destination.

  - *sendtag*  
    Send tag.

  - *recvbuf* \[out\]  
    Initial address of receive buffer.

  - *recvcount*  
    Number of elements in receive buffer.

  - *recvtype*  
    Type of elements in receive buffer.

  - *source*  
    Rank of source.

  - *recvtag*  
    Receive tag.

  - *comm*  
    Communicator.

  - *status* \[out\]  
    Status object that refers to the receive operation.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_SENDRECV(SENDBUF, SENDCOUNT, SENDTYPE, DEST, SENDTAG, RECVBUF,
            RECVCOUNT, RECVTYPE, SOURCE, RECVTAG, COMM, STATUS, IERROR)
        <type> SENDBUF(*), RECVBUF(*)
        INTEGER SENDCOUNT, SENDTYPE, DEST, SENDTAG, RECVCOUNT, RECVTYPE,
        SOURCE, RECVTAG, COMM, STATUS(MPI_STATUS_SIZE), IERROR
```

## Requirements

<table>
<colgroup>
<col  />
<col  />
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

[MPI Point to Point Functions](mpi-point-to-point-functions.md)

