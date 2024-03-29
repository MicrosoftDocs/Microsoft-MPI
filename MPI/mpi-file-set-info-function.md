---
title: MPI_File_set_info function
TOCTitle: MPI_File_set_info function
ms:assetid: 3e44f6dd-26e1-467c-981d-09cc842d2a1b
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473356(v=VS.85)
ms:contentKeyID: 59360892
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_SET_INFO
- mpif/MPI_File_set_info
- mpi/MPI_FILE_SET_INFO
dev_langs:
- C++
- C
description: Learn how to set new values for hints associated with a file using the MPI_File_set_info function on Microsoft's official site.
---

# MPI\_File\_set\_info function

Sets new values for the hints associated with a file.

## Syntax

``` c++
int MPIAPI MPI_File_set_info(
   MPI_File file,
   MPI_Info info
);
```

## Parameters

  - *file*  
    File handle.

  - *info*  
    Info object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_SET_INFO(FH, INFO, IERROR)
        INTEGER FH, INFO, IERROR
```

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

[MPI File Functions](mpi-file-functions.md)

