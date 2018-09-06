---
title: MPI_Type_create_keyval function
TOCTitle: MPI_Type_create_keyval function
ms:assetid: bd2e9269-a2cf-44e8-b2e8-b86cc5702479
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473494(v=VS.85)
ms:contentKeyID: 59361029
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_CREATE_KEYVAL
- mpif/MPI_Type_create_keyval
- mpi/MPI_TYPE_CREATE_KEYVAL
dev_langs:
- C++
- C
---

# MPI\_Type\_create\_keyval function

Creates an attribute keyval for MPI datatypes.

## Syntax

``` c++
int MPIAPI MPI_Type_create_keyval(
  _In_     MPI_Type_copy_attr_function   *type_copy_attr_fn,
  _In_     MPI_Type_delete_attr_function *type_delete_attr_fn,
  _Out_    int                           *type_keyval,
  _In_opt_ void                          *extra_state
);
```

## Parameters

  - *type\_copy\_attr\_fn* \[in\]  
    Copy callback function for *type\_keyval*.

  - *type\_delete\_attr\_fn* \[in\]  
    Delete callback function for *type\_keyval*.

  - *type\_keyval* \[out\]  
    Key value for future access.

  - *extra\_state* \[in, optional\]  
    Extra state for callback functions.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_TYPE_CREATE_KEYVAL(TYPE_COPY_ATTR_FN, TYPE_DELETE_ATTR_FN, TYPE_KEYVAL,
                EXTRA_STATE, IERROR)
        EXTERNAL TYPE_COPY_ATTR_FN, TYPE_DELETE_ATTR_FN
        INTEGER TYPE_KEYVAL, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) EXTRA_STATE

## Remarks

Default copy and delete functions are available.  These are
- **MPI\_TYPE\_NULL\_COPY\_FN**   - empty copy function
- **MPI\_TYPE\_NULL\_DELETE\_FN** - empty delete function
- **MPI\_TYPE\_DUP\_FN**          - simple dup function

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

[*MPI\_Type\_copy\_attr\_function*](mpi-type-copy-attr-function-callback-function.md)

[*MPI\_Type\_delete\_attr\_function*](mpi-type-delete-attr-function-callback-function.md)

