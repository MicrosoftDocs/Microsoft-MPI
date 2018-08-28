---
title: MPI_Type_copy_attr_function callback function
TOCTitle: MPI_Type_copy_attr_function callback function
ms:assetid: af7f651c-0da6-42e0-b7bc-5d4200f5f11f
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473486(v=VS.85)
ms:contentKeyID: 59361021
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_Type_copy_attr_function
- mpi/TYPE_COPY_ATTR_FUNCTION
- MPI_Type_copy_attr_function
- mpif/MPI_Type_copy_attr_function
- mpif/TYPE_COPY_ATTR_FUNCTION
- TYPE_COPY_ATTR_FUNCTION
dev_langs:
- C++
- C
---

# MPI\_Type\_copy\_attr\_function callback function

**MPI\_Type\_copy\_attr\_function** is a placeholder for the application-defined function name.

## Syntax

``` c++
int MPI_Type_copy_attr_function(
           MPI_Datatype olddatatype,
           int          datatype_keyval,
  _In_opt_ void         *extra_state,
  _In_     void         *attribute_val_in,
  _Out_    void         *attribute_val_out,
  _Out_    int          *flag
);
```

## Parameters

  - *olddatatype*  
    TBD

  - *datatype\_keyval*  
    TBD

  - *extra\_state* \[in, optional\]  
    TBD

  - *attribute\_val\_in* \[in\]  
    TBD

  - *attribute\_val\_out* \[out\]  
    TBD

  - *flag* \[out\]  
    TBD

## Return value

TBD

## Fortran

    SUBROUTINE TYPE_COPY_ATTR_FUNCTION(OLDTYPE, TYPE_KEYVAL, EXTRA_STATE,
                ATTRIBUTE_VAL_IN, ATTRIBUTE_VAL_OUT, FLAG, IERROR)
        INTEGER OLDTYPE, TYPE_KEYVAL, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) EXTRA_STATE,
            ATTRIBUTE_VAL_IN, ATTRIBUTE_VAL_OUT
        LOGICAL FLAG

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

