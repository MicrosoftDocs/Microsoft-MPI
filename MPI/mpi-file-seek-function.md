---
title: MPI_File_seek function
TOCTitle: MPI_File_seek function
ms:assetid: f0856c8b-b88c-47da-805e-89e1a6e3099b
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473352(v=VS.85)
ms:contentKeyID: 59360888
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_SEEK
- mpif/MPI_File_seek
- mpi/MPI_FILE_SEEK
dev_langs:
- C++
- C
description: Learn how to use the MPI_File_seek function in MS-MPI Redistributable Packages. Get syntax, parameters, and return values for successful implementation.
---

# MPI\_File\_seek function

Updates the individual file pointer.

## Syntax

``` c++
int MPIAPI MPI_File_seek(
   MPI_File   file,
   MPI_Offset offset,
   int        whence
);
```

## Parameters

  - *file*  
    File handle.

  - *offset*  
    File offset.

  - *whence*  
    Update mode.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_SEEK(FH, OFFSET, WHENCE, IERROR)
        INTEGER FH, WHENCE, IERROR
        INTEGER(KIND=MPI_OFFSET_KIND) OFFSET
```

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

[MPI File Functions](mpi-file-functions.md)

