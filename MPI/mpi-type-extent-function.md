---
title: MPI_Type_extent function
TOCTitle: MPI_Type_extent function
ms:assetid: 8b04d970-10c3-4c17-b6b4-956a41cbbc0c
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520565(v=VS.85)
ms:contentKeyID: 59361036
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_EXTENT
- mpif/MPI_Type_extent
- mpi/MPI_TYPE_EXTENT
dev_langs:
- C++
- C
---

# MPI\_Type\_extent function

This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Type\_get\_extent**](mpi-type-get-extent-function.md) function.

## Syntax

``` c++
int
MPIAPI MPI_Type_extent(
        MPI_Datatype datatype,
  _Out_ MPI_Aint     *extent
);
```

## Parameters

  - *datatype*  
    Datatype.

  - *extent* \[out\]  
    Datatype extent.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_TYPE_EXTENT(DATATYPE, LB, EXTENT, IERROR)
        INTEGER DATATYPE, IERROR
        INTEGER(KIND = MPI_ADDRESS_KIND) LB, EXTENT

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

[**MPI\_Type\_get\_extent**](mpi-type-get-extent-function.md)

