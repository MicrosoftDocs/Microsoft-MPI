---
title: MPI_Errhandler_create function
TOCTitle: MPI_Errhandler_create function
ms:assetid: 9e79d6df-6c94-44a8-aadd-e97a42dd1b6a
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473294(v=VS.85)
ms:contentKeyID: 59360840
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ERRHANDLER_CREATE
- mpif/MPI_ERRHANDLER_CREATE
- mpi/MPI_ERRHANDLER_CREATE
dev_langs:
- C++
- C
---

# MPI\_Errhandler\_create function

This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Comm\_create\_errhandler**](mpi-comm-create-errhandler-function.md) function.

## Syntax

``` c++
int MPIAPI MPI_Errhandler_create(
  _In_  MPI_Handler_function *function,
  _Out_ MPI_Errhandler       *errhandler
);
```

## Parameters

  - *function* \[in\]  
    TBD

  - *errhandler* \[out\]  
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
<td>Mpi.h</td>
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

[**MPI\_Comm\_create\_errhandler**](mpi-comm-create-errhandler-function.md)

