---
title: MPI_Comm_create_keyval function
TOCTitle: MPI_Comm_create_keyval function
ms:assetid: 13d0bf93-f8b8-4f26-bcbf-1b2a0bdab0fe
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473263(v=VS.85)
ms:contentKeyID: 59360809
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_CREATE_KEYVAL
- mpif/MPI_Comm_create_keyval
- mpi/MPI_COMM_CREATE_KEYVAL
dev_langs:
- C++
- C
description: Learn how to create a new attribute key with MPI_Comm_create_keyval function. Understand syntax, parameters, and differences between C and Fortran.
---

# MPI\_Comm\_create\_keyval function

Creates a new attribute key.

## Syntax

``` c++
int MPIAPI MPI_Comm_create_keyval(
  _In_opt_ MPI_Comm_copy_attr_function   *comm_copy_attr_fn,
  _In_opt_ MPI_Comm_delete_attr_function *comm_delete_attr_fn,
  _Out_    int                           *comm_keyval,
  _In_opt_ void                          *extra_state
);
```

## Parameters

  - *comm\_copy\_attr\_fn* \[in, optional\]  
    Copy callback function for *keyval*.

  - *comm\_delete\_attr\_fn* \[in, optional\]  
    Delete callback function for *keyval*.

  - *comm\_keyval* \[out\]  
    Key value for future access.

  - *extra\_state* \[in, optional\]  
    Extra state for callback functions.

## Return value

**MPI\_SUCCESS**

## Fortran

``` FORTRAN
    MPI_COMM_CREATE_KEYVAL(COMM_COPY_ATTR_FN, COMM_DELETE_ATTR_FN, COMM_KEYVAL,
            EXTRA_STATE, IERROR)
        EXTERNAL COMM_COPY_ATTR_FN, COMM_DELETE_ATTR_FN
        INTEGER COMM_KEYVAL, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) EXTRA_STATE
```

## Remarks

Key values are global (available for any and all communicators).

Default copy and delete functions are available.  These are
  **MPI\_COMM\_NULL\_COPY\_FN**   - empty copy function
  **MPI\_COMM\_NULL\_DELETE\_FN** - empty delete function
  **MPI\_COMM\_DUP\_FN**          - simple dup function

There are subtle differences between C and Fortran that require that the copy_fn be written in the same language from which [**MPI\_Comm\_create\_keyval**](mpi-comm-create-keyval-function.md) is called.
This should not be a problem for most users; only programers using both Fortran and C in the same program need to be sure that they follow this rule.


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

[**MPI\_Comm\_copy\_attr\_function**](mpi-comm-copy-attr-function-function.md)

[**MPI\_Comm\_delete\_attr\_function**](mpi-comm-delete-attr-function-function.md)

