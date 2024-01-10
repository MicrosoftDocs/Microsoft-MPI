---
title: MPI_Win_delete_attr_function callback function
TOCTitle: MPI_Win_delete_attr_function callback function
ms:assetid: a3882119-b24a-4d88-8127-9a79f838b265
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520600(v=VS.85)
ms:contentKeyID: 59361071
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_Win_delete_attr_function
- mpi/WIN_DELETE_ATTR_FUNCTION
- MPI_Win_delete_attr_function
- mpif/MPI_Win_delete_attr_function
- mpif/WIN_DELETE_ATTR_FUNCTION
- WIN_DELETE_ATTR_FUNCTION
dev_langs:
- C++
- C
---

# MPI\_Win\_delete\_attr\_function callback function

**MPI\_Win\_delete\_attr\_function** is a placeholder for the application-defined function name. This is a delete callback function for *win\_keyval*.

## Syntax

``` c++
int MPI_Win_delete_attr_function(
           MPI_Win win,
           int     win_keyval,
  _In_     void    *attribute_val,
  _In_opt_ void    *extra_state
);
```

## Parameters

  - *win*  
    MPI window object.

  - *win\_keyval*  
    Window key value.

  - *attribute\_val* \[in\]  
    Attribute value.

  - *extra\_state* \[in, optional\]  
    Extra state.

## Return value

If an attribute delete function returns anything other than **MPI\_SUCCESS**, then the call that caused it to be invoked (for example, [**MPI\_Win\_free**](mpi-win-free-function.md)), is erroneous.

## Fortran

``` FORTRAN
    SUBROUTINE WIN_DELETE_ATTR_FUNCTION(WIN, WIN_KEYVAL, ATTRIBUTE_VAL,
                EXTRA_STATE, IERROR)
        INTEGER WIN, WIN_KEYVAL, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) ATTRIBUTE_VAL, EXTRA_STATE
```

## Requirements

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Header</p></td>
<td>Mpi.h;
Mpif.h</td>
</tr>
</tbody>
</table>


## See also

[MPI Caching Functions](mpi-caching-functions.md)

[**MPI\_Win\_create\_keyval**](mpi-win-create-keyval-function.md)

