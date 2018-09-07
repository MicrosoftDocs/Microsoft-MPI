---
title: MPI_Type_hvector function
TOCTitle: MPI_Type_hvector function
ms:assetid: 25ce3e68-95d3-4d83-ac36-16ed76c914dd
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520575(v=VS.85)
ms:contentKeyID: 59361046
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_HVECTOR
- mpif/MPI_Type_hvector
- mpi/MPI_TYPE_HVECTOR
dev_langs:
- C++
- C
---

# MPI\_Type\_hvector function

This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Type\_create\_hvector**](mpi-type-create-hvector-function.md) function.

## Syntax

``` c++
int
MPIAPI MPI_Type_hvector(
        int          count,
        int          blocklength,
        MPI_Aint     stride,
        MPI_Datatype oldtype,
  _Out_ MPI_Datatype *newtype
);
```

## Parameters

  - *count*  
    Number of blocks.

  - *blocklength*  
    Number of elements in each block.

  - *stride*  
    Number of bytes between start of each block.

  - *oldtype*  
    Old datatype.

  - *newtype* \[out\]  
    New datatype.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_TYPE_HVECTOR(COUNT, BLOCKLENGTH, STRIDE, OLDTYPE, NEWTYPE,
        IERROR)
        INTEGER COUNT, BLOCKLENGTH, OLDTYPE, NEWTYPE, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) STRIDE

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

[**MPI\_Type\_create\_hvector**](mpi-type-create-hvector-function.md)

