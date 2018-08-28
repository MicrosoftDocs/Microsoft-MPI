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
---

# MPI\_Sendrecv\_replace function

TBD

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
    TBD

  - *count*  
    TBD

  - *datatype*  
    TBD

  - *dest*  
    TBD

  - *sendtag*  
    TBD

  - *source*  
    TBD

  - *recvtag*  
    TBD

  - *comm*  
    TBD

  - *status* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_SENDRECV_REPLACE(BUF, COUNT, DATATYPE, DEST, SENDTAG, SOURCE, RECVTAG,
            COMM, STATUS, IERROR)
        <type> BUF(*)
        INTEGER COUNT, DATATYPE, DEST, SENDTAG, SOURCE, RECVTAG, COMM,
        STATUS(MPI_STATUS_SIZE), IERROR

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

[MPI Point to Point Functions](mpi-point-to-point-functions.md)

