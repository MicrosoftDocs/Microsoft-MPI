---
title: MPI_Intercomm_merge function
TOCTitle: MPI_Intercomm_merge function
ms:assetid: 09f063e6-f21f-448d-b8fe-c7509aecc0bd
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473423(v=VS.85)
ms:contentKeyID: 59360959
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_INTERCOMM_MERGE
- mpif/MPI_Intercomm_merge
- mpi/MPI_INTERCOMM_MERGE
dev_langs:
- C++
- C
description: Learn how to create an intracommunicator from an intercommunicator using MPI_Intercomm_merge function on Microsoft's official site.
---

# MPI\_Intercomm\_merge function

Creates an intracommuncator from an intercommunicator.

## Syntax

``` c++
int MPIAPI MPI_Intercomm_merge(
        MPI_Comm intercomm,
        int      high,
  _Out_ MPI_Comm *newintracomm
);
```

## Parameters

  - *intercomm*  
    Intercommunicator.

  - *high*  
    Used to order the groups within comm when creating the new communicator.  This is a boolean value; the group that sets high true has its processes ordered *after* the group that sets this value to false.  If all processes in the intercommunicator provide the same value, the choice of which group is ordered first is arbitrary.

  - *newintracomm* \[out\]  
    Created intracommunicator.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_INTERCOMM_MERGE(INTERCOMM, HIGH, NEWINTRACOMM, IERROR)
        INTEGER INTERCOMM, NEWINTRACOMM, IERROR
        LOGICAL HIGH
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

[MPI Communicator Functions](mpi-communicator-functions.md)

