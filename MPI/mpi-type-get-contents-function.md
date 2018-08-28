---
title: MPI_Type_get_contents function
TOCTitle: MPI_Type_get_contents function
ms:assetid: 1e25a15b-cc5a-4584-b130-29b742c84753
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520569(v=VS.85)
ms:contentKeyID: 59361040
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_GET_CONTENTS
- mpif/MPI_Type_get_contents
- mpi/MPI_TYPE_GET_CONTENTS
dev_langs:
- C++
- C
---

# MPI\_Type\_get\_contents function

TBD

## Syntax

``` c++
int MPIAPI MPI_Type_get_contents(
   MPI_Datatype                          datatype,
   int                                   max_integers,
   int                                   max_addresses,
   int                                   max_datatypes,
   _Out_cap_(max_integers) int           array_of_integers[],
   _Out_cap_(max_addresses) MPI_Aint     array_of_addresses[],
   _Out_cap_(max_datatypes) MPI_Datatype array_of_datatypes[]
);
```

## Parameters

  - *datatype*  
    TBD

  - *max\_integers*  
    TBD

  - *max\_addresses*  
    TBD

  - *max\_datatypes*  
    TBD

  - *array\_of\_integers*  
    TBD

  - *array\_of\_addresses*  
    TBD

  - *array\_of\_datatypes*  
    TBD

## Return value

TBD

## Fortran

    MPI_TYPE_GET_CONTENTS(DATATYPE, MAX_INTEGERS, MAX_ADDRESSES, MAX_DATATYPES,
                ARRAY_OF_INTEGERS, ARRAY_OF_ADDRESSES, ARRAY_OF_DATATYPES, IERROR)
        INTEGER DATATYPE, MAX_INTEGERS, MAX_ADDRESSES, MAX_DATATYPES,
        ARRAY_OF_INTEGERS(*), ARRAY_OF_DATATYPES(*), IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) ARRAY_OF_ADDRESSES(*)

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

[MPI Datatype Functions](mpi-datatype-functions.md)

