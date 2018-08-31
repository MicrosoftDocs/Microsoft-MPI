---
title: MPI_File_preallocate function
TOCTitle: MPI_File_preallocate function
ms:assetid: 0e5cdcbc-e7ab-43fd-83f5-c67762e0b19e
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473329(v=VS.85)
ms:contentKeyID: 59360875
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_PREALLOCATE
- mpif/MPI_File_preallocate
- mpi/MPI_FILE_PREALLOCATE
dev_langs:
- C++
- C
---

# MPI\_File\_preallocate function

Preallocates storage space for a file.

## Syntax

``` c++
int MPIAPI MPI_File_preallocate(
   MPI_File   file,
   MPI_Offset size
);
```

## Parameters

  - *file*  
    File handle.

  - *size*  
    Size to preallocate.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_FILE_PREALLOCATE(FH, SIZE, IERROR)
        INTEGER FH, IERROR
        INTEGER(KIND=MPI_OFFSET_KIND) SIZE

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

