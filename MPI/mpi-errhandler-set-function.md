---
title: MPI_Errhandler_set function
TOCTitle: MPI_Errhandler_set function
ms:assetid: fdf998d3-37a5-423c-b853-ac797dffa440
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473297(v=VS.85)
ms:contentKeyID: 59360843
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ERRHANDLER_SET
- mpif/MPI_Errhandler_set
- mpi/MPI_ERRHANDLER_SET
dev_langs:
- C++
- C
---

# MPI\_Errhandler\_set function

This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Comm\_set\_errhandler**](mpi-comm-set-errhandler-function.md) function.

## Syntax

``` c++
int
MPIAPI MPI_Errhandler_set(
   MPI_Comm       comm,
   MPI_Errhandler errhandler
);
```

## Parameters

  - *comm*  
    TBD

  - *errhandler*  
    TBD

## Return value

TBD

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

[MPI Management Functions](mpi-management-functions.md)

[**MPI\_Comm\_set\_errhandler**](mpi-comm-set-errhandler-function.md)

