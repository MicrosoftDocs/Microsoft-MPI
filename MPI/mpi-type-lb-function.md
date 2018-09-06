---
title: MPI_Type_lb function
TOCTitle: MPI_Type_lb function
ms:assetid: d9cc896e-ed0f-4625-94cd-c59a95da1705
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520577(v=VS.85)
ms:contentKeyID: 59361048
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_LB
- mpif/MPI_Type_lb
- mpi/MPI_TYPE_LB
dev_langs:
- C++
- C
---

# MPI\_Type\_lb function

This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Type\_get\_extent**](mpi-type-get-extent-function.md) function.

## Syntax

``` c++
int
MPIAPI MPI_Type_lb(
        MPI_Datatype datatype,
  _Out_ MPI_Aint     *displacement
);
```

## Parameters

  - *datatype*  
    Datatype.

  - *displacement* \[out\]  
    Displacement of lower bound from origin, in bytes.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` 
```

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

