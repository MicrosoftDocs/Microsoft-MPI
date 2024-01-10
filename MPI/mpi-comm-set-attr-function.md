---
title: MPI_Comm_set_attr function
TOCTitle: MPI_Comm_set_attr function
ms:assetid: c2a64e32-631d-4865-8805-6c70cf4fb4db
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473280(v=VS.85)
ms:contentKeyID: 59360826
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_SET_ATTR
- mpif/MPI_Comm_set_attr
- mpi/MPI_COMM_SET_ATTR
dev_langs:
- C++
- C
---

# MPI\_Comm\_set\_attr function

Stores attribute value associated with a key.

## Syntax

``` c++
int MPIAPI MPI_Comm_set_attr(
       MPI_Comm comm,
       int      comm_keyval,
  _In_ void     *attribute_val
);
```

## Parameters

  - *comm*  
    Communicator to which attribute will be attached.

  - *comm\_keyval*  
    Key value, as returned by  [**MPI\_Comm\_create\_keyval**](mpi-comm-create-keyval-function.md).

  - *attribute\_val* \[in\]  
    Attribute value.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMM_SET_ATTR(COMM, COMM_KEYVAL, ATTRIBUTE_VAL, IERROR)
        INTEGER COMM, COMM_KEYVAL, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) ATTRIBUTE_VAL
```

## Remarks

Values of the permanent attributes **MPI\_TAG\_UB**, **MPI\_HOST**, **MPI\_IO**, **MPI\_WTIME\_IS\_GLOBAL**, **MPI\_UNIVERSE\_SIZE**, **MPI\_LASTUSEDCODE**, and **MPI\_APPNUM** may not be changed.

The datatype of the attribute value depends on whether C, C++, or Fortran is being used. In C and C++, an attribute value is a void pointer; in Fortran, it is an address-sized integer.

If an attribute is already present, the delete function (specified when the corresponding keyval was created) will be called.

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

