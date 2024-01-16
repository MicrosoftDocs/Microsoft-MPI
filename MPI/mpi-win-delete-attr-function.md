---
title: MPI_Win_delete_attr function
TOCTitle: MPI_Win_delete_attr function
ms:assetid: fcc481c2-b8ea-4deb-a5aa-5f52daf786f3
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520599(v=VS.85)
ms:contentKeyID: 59361070
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_DELETE_ATTR
- mpif/MPI_Win_delete_attr
- mpi/MPI_WIN_DELETE_ATTR
dev_langs:
- C++
- C
---

# MPI\_Win\_delete\_attr function

Deletes an attribute value associated with a key on a MPI window object.

## Syntax

``` c++
int MPIAPI MPI_Win_delete_attr(
   MPI_Win win,
   int     win_keyval
);
```

## Parameters

  - *win*  
    Window from which the attribute is deleted.

  - *win\_keyval*  
    Key value.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_DELETE_ATTR(WIN, WIN_KEYVAL, IERROR)
        INTEGER WIN, WIN_KEYVAL, IERROR
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

[MPI Caching Functions](mpi-caching-functions.md)

