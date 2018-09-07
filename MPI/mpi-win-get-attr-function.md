---
title: MPI_Win_get_attr function
TOCTitle: MPI_Win_get_attr function
ms:assetid: 772d60fb-b2f0-4498-b39d-86b25be9450d
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520605(v=VS.85)
ms:contentKeyID: 59361076
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_GET_ATTR
- mpif/MPI_Win_get_attr
- mpi/MPI_WIN_GET_ATTR
dev_langs:
- C++
- C
---

# MPI\_Win\_get\_attr function

Get attribute cached on an MPI window object.

## Syntax

``` c++
int MPIAPI MPI_Win_get_attr(
        MPI_Win win,
        int     win_keyval,
  _Out_ void    *attribute_val,
  _Out_ int     *flag
);
```

## Parameters

  - *win*  
    Window to which the attribute is attached.

  - *win\_keyval*  
    Key value.

  - *attribute\_val* \[out\]  
    Attribute value, unless *flag* is false.

  - *flag* \[out\]  
    False if no attribute is associated with the key.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_WIN_GET_ATTR(WIN, WIN_KEYVAL, ATTRIBUTE_VAL, FLAG, IERROR)
        INTEGER WIN, WIN_KEYVAL, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) ATTRIBUTE_VAL
        LOGICAL FLAG

## Remarks

The following attributes are predefined for all MPI Window objects:

- **MPI\_WIN\_BASE** - window base address.
- **MPI\_WIN\_SIZE** - window size, in bytes.
- **MPI\_WIN\_DISP\_UNIT** - displacement unit associated with the window.
- **MPI\_WIN\_CREATE\_FLAVOR** - how the window was created.
- **MPI\_WIN\_MODEL** - memory model for the window.

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

