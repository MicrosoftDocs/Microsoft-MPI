---
title: MPI_File_c2f function
TOCTitle: MPI_File_c2f function
ms:assetid: 12db8e3e-f4df-48c2-b780-94cef9ef3baa
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473303(v=VS.85)
ms:contentKeyID: 59360849
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_File_c2f
- MPI_File_c2f
- mpif/MPI_File_c2f
dev_langs:
- C++
- C
---

# MPI\_File\_c2f function

Translates a C file handle to a Fortran file handle.

## Syntax

``` c++
MPI_Fint MPIAPI MPI_File_c2f(
   MPI_File file
);
```

## Parameters

  - *file*  
    C file handle.

## Return value

Fortran file handle.

## Requirements

<table>
<colgroup>
<col/>
<col/>
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

