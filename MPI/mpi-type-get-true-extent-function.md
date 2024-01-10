---
title: MPI_Type_get_true_extent function
TOCTitle: MPI_Type_get_true_extent function
ms:assetid: a55f4c95-e51f-48ac-a965-ccd403c9bd71
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520573(v=VS.85)
ms:contentKeyID: 59361044
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_GET_TRUE_EXTENT
- mpif/MPI_Type_get_true_extent
- mpi/MPI_TYPE_GET_TRUE_EXTENT
dev_langs:
- C++
- C
---

# MPI\_Type\_get\_true\_extent function

Get the true lower bound and extent for a datatype.

## Syntax

``` c++
int MPIAPI MPI_Type_get_true_extent(
        MPI_Datatype datatype,
  _Out_ MPI_Aint     *true_lb,
  _Out_ MPI_Aint     *true_extent
);
```

## Parameters

  - *datatype*  
    Datatype to get information on.

  - *true\_lb* \[out\]  
    True lower bound of datatype.

  - *true\_extent* \[out\]  
    True size of datatype.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_TYPE_GET_TRUE_EXTENT(DATATYPE, TRUE_LB, TRUE_EXTENT, IERROR)
        INTEGER DATATYPE, IERROR
        INTEGER(KIND = MPI_ADDRESS_KIND) TRUE_LB, TRUE_EXTENT
```

## Remarks

*true\_lb* returns the offset of the lowest unit of store which is addressed by the datatype, i.e., the lower bound of the corresponding typemap, ignoring explicit lower bound markers. *true\_extent* returns the true size of the datatype, i.e., the extent of the corresponding typemap, ignoring explicit lower bound and upper bound markers, and performing no rounding for alignment.

## Requirements

<table>
<colgroup>
<col  />
<col  />
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

