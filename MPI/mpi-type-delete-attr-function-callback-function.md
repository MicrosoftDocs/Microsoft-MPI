---
title: MPI_Type_delete_attr_function callback function
TOCTitle: MPI_Type_delete_attr_function callback function
ms:assetid: 51e6cd99-404f-4ede-9b92-e87ff9469053
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520563(v=VS.85)
ms:contentKeyID: 59361034
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_Type_delete_attr_function
- mpi/TYPE_DELETE_ATTR_FUNCTION
- MPI_Type_delete_attr_function
- mpif/MPI_Type_delete_attr_function
- mpif/TYPE_DELETE_ATTR_FUNCTION
- TYPE_DELETE_ATTR_FUNCTION
dev_langs:
- C++
- C
---

# MPI\_Type\_delete\_attr\_function callback function

**MPI\_Type\_delete\_attr\_function** is a placeholder for the application-defined function name.

## Syntax

``` c++
int MPI_Type_delete_attr_function(
           MPI_Datatype datatype,
           int          datatype_keyval,
  _In_     void         *attribute_val,
  _In_opt_ void         *extra_state
);
```

## Parameters

  - *datatype*  
    Datatype.

  - *datatype\_keyval*  
    Key value.

  - *attribute\_val* \[in\]  
    Attribute value.

  - *extra\_state* \[in, optional\]  
    Extra state.

## Return value

If an attribute delete function returns something other than **MPI\_SUCCESS**, then the call that caused it to be invoked (for example, [**MPI\_Type\_free**](mpi-type-free-function.md)), is erroneous.

## Fortran

    SUBROUTINE TYPE_DELETE_ATTR_FUNCTION(DATATYPE, TYPE_KEYVAL, ATTRIBUTE_VAL,
                EXTRA_STATE, IERROR)
        INTEGER DATATYPE, TYPE_KEYVAL, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) ATTRIBUTE_VAL, EXTRA_STATE

## Requirements

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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

[**MPI\_Type\_create\_keyval**](mpi-type-create-keyval-function.md)

