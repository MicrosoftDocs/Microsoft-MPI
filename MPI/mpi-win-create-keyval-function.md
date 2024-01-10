---
title: MPI_Win_create_keyval function
TOCTitle: MPI_Win_create_keyval function
ms:assetid: 6c871be1-55e6-4aa9-bd4b-5c9b99ba953c
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520598(v=VS.85)
ms:contentKeyID: 59361069
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_CREATE_KEYVAL
- mpif/MPI_Win_create_keyval
- mpi/MPI_WIN_CREATE_KEYVAL
dev_langs:
- C++
- C
---

# MPI\_Win\_create\_keyval function

Creates an attribute keyval for MPI window objects.

## Syntax

``` c++
int MPIAPI MPI_Win_create_keyval(
  _In_     MPI_Win_copy_attr_function   *win_copy_attr_fn,
  _In_     MPI_Win_delete_attr_function *win_delete_attr_fn,
  _Out_    int                          *win_keyval,
  _In_opt_ void                         *extra_state
);
```

## Parameters

  - *win\_copy\_attr\_fn* \[in\]  
    Copy callback function for *win\_keyval*.

  - *win\_delete\_attr\_fn* \[in\]  
    Delete callback function for *win\_keyval*.

  - *win\_keyval* \[out\]  
    Key value for future access.

  - *extra\_state* \[in, optional\]  
    Extra state for callback functions.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_CREATE_KEYVAL(WIN_COPY_ATTR_FN, WIN_DELETE_ATTR_FN, WIN_KEYVAL,
                EXTRA_STATE, IERROR)
        EXTERNAL WIN_COPY_ATTR_FN, WIN_DELETE_ATTR_FN
        INTEGER WIN_KEYVAL, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) EXTRA_STATE
```

## Remarks

Default copy and delete functions are available.  These are
- **MPI\_WIN\_NULL\_COPY\_FN**   - empty copy function
- **MPI\_WIN\_NULL\_DELETE\_FN** - empty delete function
- **MPI\_WIN\_DUP\_FN**          - simple dup function


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

[*MPI\_Win\_delete\_attr\_function*](mpi-win-delete-attr-function-callback-function.md)

[*MPI\_Win\_copy\_attr\_function*](mpi-win-copy-attr-function-callback-function.md)

