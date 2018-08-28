---
title: MPI_Intercomm_create function
TOCTitle: MPI_Intercomm_create function
ms:assetid: 6b40ca68-4d69-4445-b723-e0ee79770ad0
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473422(v=VS.85)
ms:contentKeyID: 59360958
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_INTERCOMM_CREATE
- mpif/MPI_Intercomm_create
- mpi/MPI_INTERCOMM_CREATE
dev_langs:
- C++
- C
---

# MPI\_Intercomm\_create function

TBD

## Syntax

``` c++
int MPIAPI MPI_Intercomm_create(
        MPI_Comm local_comm,
        int      local_leader,
        MPI_Comm peer_comm,
        int      remote_leader,
        int      tag,
  _Out_ MPI_Comm *newintercomm
);
```

## Parameters

  - *local\_comm*  
    TBD

  - *local\_leader*  
    TBD

  - *peer\_comm*  
    TBD

  - *remote\_leader*  
    TBD

  - *tag*  
    TBD

  - *newintercomm* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_INTERCOMM_CREATE(LOCAL_COMM, LOCAL_LEADER, PEER_COMM, REMOTE_LEADER, 
            TAG, NEWINTERCOMM, IERROR)
        INTEGER LOCAL_COMM, LOCAL_LEADER, PEER_COMM, REMOTE_LEADER, TAG,
        NEWINTERCOMM, IERROR

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

[MPI Communicator Functions](mpi-communicator-functions.md)

