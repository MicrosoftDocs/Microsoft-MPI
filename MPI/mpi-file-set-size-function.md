---
title: MPI_File_set_size function
TOCTitle: MPI_File_set_size function
ms:assetid: b1485a17-c2f1-4438-bd4c-197dda17755f
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473357(v=VS.85)
ms:contentKeyID: 59360893
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_SET_SIZE
- mpif/MPI_File_set_size
- mpi/MPI_FILE_SET_SIZE
dev_langs:
- C++
- C
description: Learn Microsoft MPI File Set Size Function: Easily set file size, truncate or expand files with MPI_SUCCESS. Maximize efficiency today.
---

# MPI\_File\_set\_size function

Sets the file size.

## Syntax

``` c++
int MPIAPI MPI_File_set_size(
   MPI_File   file,
   MPI_Offset size
);
```

## Parameters

  - *file*  
    File handle.

  - *size*  
    Size to truncate or expand file.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_SET_SIZE(FH, SIZE, IERROR)
        INTEGER FH, IERROR
        INTEGER(KIND=MPI_OFFSET_KIND) SIZE
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

[MPI File Functions](mpi-file-functions.md)

