---
title: MPI_Win_get_group function
TOCTitle: MPI_Win_get_group function
ms:assetid: bfab8339-31c4-4a46-87eb-fec77693d7c7
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520607(v=VS.85)
ms:contentKeyID: 59361078
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_GET_GROUP
- mpif/MPI_Win_get_group
- mpi/MPI_WIN_GET_GROUP
dev_langs:
- C++
- C
---

# MPI\_Win\_get\_group function

Gets the MPI Group of the window object.

## Syntax

``` c++
int MPIAPI MPI_Win_get_group(
        MPI_Win   win,
  _Out_ MPI_Group *group
);
```

## Parameters

  - *win*  
    Window object.

  - *group* \[out\]  
    Group of processes that share access to the window.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_GET_GROUP(WIN, GROUP, IERROR)
        INTEGER WIN, GROUP, IERROR
```

## Remarks

The group is a duplicate of the group from the communicator used to create the MPI window, and should be freed with [**MPI\_Group\_free**](mpi-group-free-function.md) when it is no longer needed.  This group can be used to form the group of neighbors for the routines [**MPI\_Win\_post**](mpi-win-post-function.md) and [**MPI\_Win\_start**](mpi-win-start-function.md).

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

[MPI One-Sided Communications Functions](mpi-one-sided-communications-functions.md)

