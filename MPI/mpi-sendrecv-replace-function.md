---
title: MPI_Sendrecv_replace function
TOCTitle: MPI_Sendrecv_replace function
ms:assetid: 6b8cfc50-a75c-44cf-8106-5935abead2ef
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473469(v=VS.85)
ms:contentKeyID: 59361004
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_SENDRECV_REPLACE
- mpif/MPI_Sendrecv_replace
- mpi/MPI_SENDRECV_REPLACE
dev_langs:
- C++
- C
description: Explore MPI_Sendrecv_replace function on Microsoft's learning platform. Understand syntax, parameters, return values, and related requirements.
---

# MPI\_Sendrecv\_replace function

Sends and receives using a single buffer.

## Syntax

``` c++
int MPIAPI MPI_Sendrecv_replace(
        _Inout_ void *buf,
        int          count,
        MPI_Datatype datatype,
        int          dest,
        int          sendtag,
        int          source,
        int          recvtag,
        MPI_Comm     comm,
  _Out_ MPI_Status   *status
);
```

## Parameters

  - *buf*  
    Initial address of send and receive buffer.

  - *count*  
    Number of elements in send and receive buffer.

  - *datatype*  
    Type of elements in send and receive buffer.

  - *dest*  
    Rank of destination.

  - *sendtag*  
    Send message tag.

  - *source*  
    Rank of source.

  - *recvtag*  
    Receive message tag.

  - *comm*  
    Communicator.

  - *status* \[out\]  
    Status object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_SENDRECV_REPLACE(BUF, COUNT, DATATYPE, DEST, SENDTAG, SOURCE, RECVTAG,
            COMM, STATUS, IERROR)
        <type> BUF(*)
        INTEGER COUNT, DATATYPE, DEST, SENDTAG, SOURCE, RECVTAG, COMM,
        STATUS(MPI_STATUS_SIZE), IERROR
```

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

[MPI Point to Point Functions](mpi-point-to-point-functions.md)

