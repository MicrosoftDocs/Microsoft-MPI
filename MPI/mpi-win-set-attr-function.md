﻿---
title: MPI_Win_set_attr function
TOCTitle: MPI_Win_set_attr function
ms:assetid: 971c484a-65d6-4cc8-8683-4f13a10f7627
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520611(v=VS.85)
ms:contentKeyID: 59361082
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_SET_ATTR
- mpif/MPI_Win_set_attr
- mpi/MPI_WIN_SET_ATTR
dev_langs:
- C++
- C
---

# MPI\_Win\_set\_attr function

Stores attribute value associated with a key.

## Syntax

``` c++
int MPIAPI MPI_Win_set_attr(
       MPI_Win win,
       int     win_keyval,
  _In_ void    *attribute_val
);
```

## Parameters

  - *win*  
    MPI window object to which attribute will be attached.

  - *win\_keyval*  
    Key value, as returned by [**MPI\_Win\_create\_keyval**](mpi-win-create-keyval-function.md).

  - *attribute\_val* \[in\]  
    Attribute value.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_SET_ATTR(WIN, WIN_KEYVAL, ATTRIBUTE_VAL, IERROR)
        INTEGER WIN, WIN_KEYVAL, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) ATTRIBUTE_VAL
```

## Remarks

The datatype of the attribute value depends on whether C or Fortran is being used. In C, an attribute value is a void pointer; in Fortran, it is an address-sized integer.

If an attribute is already present, the delete function (specified when the corresponding keyval was created) will be called.

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

[MPI Caching Functions](mpi-caching-functions.md)

