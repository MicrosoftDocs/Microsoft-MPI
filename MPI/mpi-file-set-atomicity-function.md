---
title: MPI_File_set_atomicity function
TOCTitle: MPI_File_set_atomicity function
ms:assetid: f53af688-ddd0-4eb0-a83a-2d31b01d05d1
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473354(v=VS.85)
ms:contentKeyID: 59360890
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_SET_ATOMICITY
- mpif/MPI_File_set_atomicity
- mpi/MPI_FILE_SET_ATOMICITY
dev_langs:
- C++
- C
---

# MPI\_File\_set\_atomicity function

TBD

## Syntax

``` c++
int MPIAPI MPI_File_set_atomicity(
   MPI_File file,
   int      flag
);
```

## Parameters

  - *file*  
    TBD

  - *flag*  
    TBD

## Return value

TBD

## Fortran

    MPI_FILE_SET_ATOMICITY(FH, FLAG, IERROR)
        INTEGER FH, IERROR
        LOGICAL FLAG

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

[MPI File Functions](mpi-file-functions.md)

