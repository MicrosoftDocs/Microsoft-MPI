---
title: MPI_Comm_delete_attr_function function
TOCTitle: MPI_Comm_delete_attr_function function
ms:assetid: d8b778cb-c354-4361-8d7a-0dc0f3209cdf
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473265(v=VS.85)
ms:contentKeyID: 59360811
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- COMM_DELETE_ATTR_FUNCTION
- mpi/COMM_DELETE_ATTR_FUNCTION
- mpi/MPI_Comm_delete_attr_function
- MPI_Comm_delete_attr_function
- mpif/COMM_DELETE_ATTR_FUNCTION
- mpif/MPI_Comm_delete_attr_function
dev_langs:
- C++
- C
---

# MPI\_Comm\_delete\_attr\_function function

**MPI\_Comm\_delete\_attr\_function** is a placeholder for the application-defined function name.

## Syntax

``` c++
int MPI_Comm_delete_attr_function(
           MPI_Comm comm,
           int      comm_keyval,
  _In_     void     *attribute_val,
  _In_opt_ void     *extra_state
);
```

## Parameters

  - *comm*  
    Communicator.

  - *comm\_keyval*  
    Key value.

  - *attribute\_val* \[in\]  
    Pointer to attribute value.

  - *extra\_state* \[in, optional\]  
    Extra state.

## Return value

The function returns **MPI\_SUCCESS** on success and an error code on failure (in which case [**MPI\_Comm\_free**](mpi-comm-free-function.md) will fail).

## Fortran

``` FORTRAN
    SUBROUTINE COMM_DELETE_ATTR_FUNCTION(COMM, COMM_KEYVAL, ATTRIBUTE_VAL,
                EXTRA_STATE, IERROR)
        INTEGER COMM, COMM_KEYVAL, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) ATTRIBUTE_VAL, EXTRA_STATE
```

## Remarks

This function is invoked when a communicator is deleted by [**MPI\_Comm\_free**](mpi-comm-free-function.md) or when a call is made explicitly to [**MPI\_Comm\_delete\_attr**](mpi-comm-delete-attr-function.md).

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

[**MPI\_Comm\_create\_keyval**](mpi-comm-create-keyval-function.md)

