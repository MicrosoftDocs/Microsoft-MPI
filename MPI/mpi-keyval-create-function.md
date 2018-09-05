---
title: MPI_Keyval_create function
TOCTitle: MPI_Keyval_create function
ms:assetid: 427928ee-84a3-4bbb-9c03-f1b32f5c9b42
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473430(v=VS.85)
ms:contentKeyID: 59360966
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_KEYVAL_CREATE
- mpif/MPI_Keyval_create
- mpi/MPI_KEYVAL_CREATE
dev_langs:
- C++
- C
---

# MPI\_Keyval\_create function

This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Comm\_create\_keyval**](mpi-comm-create-keyval-function.md) function.

## Syntax

``` c++
int
MPIAPI MPI_Keyval_create(
  _In_     MPI_Copy_function   *copy_fn,
  _In_     MPI_Delete_function *delete_fn,
  _Out_    int                 *keyval,
  _In_opt_ void                *extra_state
);
```

## Parameters

  - *copy\_fn* \[in\]  
    Copy callback function for *keyval*.

  - *delete\_fn* \[in\]  
    Delete callback function for *keyval*.

  - *keyval* \[out\]  
    Key value for future access.

  - *extra\_state* \[in, optional\]  
    Extra state for callback functions.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_KEYVAL_CREATE(COPY_FN, DELETE_FN, KEYVAL, EXTRA_STATE, IERROR)
        EXTERNAL COPY_FN, DELETE_FN
        INTEGER KEYVAL, EXTRA_STATE, IERROR

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

[**MPI\_Comm\_create\_keyval**](mpi-comm-create-keyval-function.md)

