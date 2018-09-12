---
title: MPI_File_sync function
TOCTitle: MPI_File_sync function
ms:assetid: b18288ed-e627-43a1-826a-bc80243500bc
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473359(v=VS.85)
ms:contentKeyID: 59360895
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_SYNC
- mpif/MPI_File_sync
- mpi/MPI_FILE_SYNC
dev_langs:
- C++
- C
---

# MPI\_File\_sync function

Causes all previous writes to be transferred to the storage device.

## Syntax

``` c++
int MPIAPI MPI_File_sync(
   MPI_File file
);
```

## Parameters

  - *file*  
    File handle.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_SYNC(FH, IERROR)
        INTEGER FH, IERROR
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

