---
title: MPI_File_get_group function
TOCTitle: MPI_File_get_group function
ms:assetid: d4fb24d9-b010-4d3e-8a0b-d7269ebd6e38
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473315(v=VS.85)
ms:contentKeyID: 59360861
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_GET_GROUP
- mpif/MPI_File_get_group
- mpi/MPI_FILE_GET_GROUP
dev_langs:
- C++
- C
description: Learn about the MPI_File_get_group function on Microsoft's official site. Understand its syntax, parameters, return values, and related requirements.
---

# MPI\_File\_get\_group function

Returns the group of processes that opened the file.

## Syntax

``` c++
int MPIAPI MPI_File_get_group(
        MPI_File  file,
  _Out_ MPI_Group *group
);
```

## Parameters

  - *file*  
    File handle.

  - *group* \[out\]  
    Group that opened the file.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_GET_GROUP(FH, GROUP, IERROR)
        INTEGER FH, GROUP, IERROR
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

