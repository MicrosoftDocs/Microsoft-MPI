---
title: MPI_Win_get_name function
TOCTitle: MPI_Win_get_name function
ms:assetid: d50ea5e1-e23e-4c33-9213-af2676e25106
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520608(v=VS.85)
ms:contentKeyID: 59361079
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_GET_NAME
- mpif/MPI_Win_get_name
- mpi/MPI_WIN_GET_NAME
dev_langs:
- C++
- C
---

# MPI\_Win\_get\_name function

Gets the print name associated with the MPI window object.

## Syntax

``` c++
int MPIAPI MPI_Win_get_name(
        MPI_Win                                                     win,
        _Out_z_cap_post_count_(MPI_MAX_OBJECT_NAME,*resultlen) char *win_name,
  _Out_ int                                                         *resultlen
);
```

## Parameters

  - *win*  
    Window whose name is to be returned.

  - *win\_name*  
    The name previously stored on the window, or a empty string if no such name exists.

  - *resultlen* \[out\]  
    Length of returned name.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_WIN_GET_NAME(WIN, WIN_NAME, RESULTLEN, IERROR)
        INTEGER WIN, RESULTLEN, IERROR
        CHARACTER*(*) WIN_NAME

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

[MPI Miscellaneous Functions](mpi-miscellaneous-functions.md)

