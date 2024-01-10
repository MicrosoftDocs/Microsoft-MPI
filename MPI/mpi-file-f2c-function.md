---
title: MPI_File_f2c function
TOCTitle: MPI_File_f2c function
ms:assetid: 06be8e19-475c-4560-858f-cc5e92104e1d
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473309(v=VS.85)
ms:contentKeyID: 59360855
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_File_f2c
- MPI_File_f2c
- mpif/MPI_File_f2c
dev_langs:
- C++
- C
---

# MPI\_File\_f2c function

Translates a Fortran file handle to a C file handle.

## Syntax

``` c++
MPI_File MPIAPI MPI_File_f2c(
   MPI_Fint file
);
```

## Parameters

  - *file*  
    Fortran file handle.

## Return value

C file handle.

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

[MPI Miscellaneous Functions](mpi-miscellaneous-functions.md)

