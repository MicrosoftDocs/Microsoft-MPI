---
title: MPI_Type_set_attr function
TOCTitle: MPI_Type_set_attr function
ms:assetid: 209ea154-8c25-46ec-8bf9-eca8e5e26b42
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520579(v=VS.85)
ms:contentKeyID: 59361050
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_SET_ATTR
- mpif/MPI_Type_set_attr
- mpi/MPI_TYPE_SET_ATTR
dev_langs:
- C++
- C
---

# MPI\_Type\_set\_attr function

Stores attribute value associated with a key.

## Syntax

``` c++
int MPIAPI MPI_Type_set_attr(
       MPI_Datatype type,
       int          type_keyval,
  _In_ void         *attribute_val
);
```

## Parameters

  - *type*  
    MPI Datatype to which attribute will be attached.

  - *type\_keyval*  
    Key value, as returned by  [**MPI\_Type\_create\_keyval**](mpi-type-create-keyval-function.md).

  - *attribute\_val* \[in\]  
    Attribute value.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_TYPE_SET_ATTR(DATATYPE, TYPE_KEYVAL, ATTRIBUTE_VAL, IERROR)
        INTEGER DATATYPE, TYPE_KEYVAL, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) ATTRIBUTE_VAL

## Remarks

The datatype of the attribute value depends on whether C or Fortran is being used. In C, an attribute value is a void pointer; in Fortran, it is an address-sized integer.

If an attribute is already present, the delete function (specified when the corresponding keyval was created) will be called.

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

