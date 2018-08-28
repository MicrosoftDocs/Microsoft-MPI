---
title: MPI_Keyval_free function
TOCTitle: MPI_Keyval_free function
ms:assetid: 1fe7db0c-2283-4cf4-ba4f-a7d80563cea1
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473431(v=VS.85)
ms:contentKeyID: 59360967
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_KEYVAL_FREE
- mpif/MPI_Keyval_free
- mpi/MPI_KEYVAL_FREE
dev_langs:
- C++
- C
---

# MPI\_Keyval\_free function

This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Comm\_free\_keyval**](mpi-comm-free-keyval-function.md) function.

## Syntax

``` c++
int
MPIAPI MPI_Keyval_free(
   _Inout_ int *keyval
);
```

## Parameters

  - *keyval*  
    TBD

## Return value

TBD

## Fortran

    MPI_KEYVAL_FREE(KEYVAL, IERROR)
        INTEGER KEYVAL, IERROR

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

[**MPI\_Comm\_free\_keyval**](mpi-comm-free-keyval-function.md)

