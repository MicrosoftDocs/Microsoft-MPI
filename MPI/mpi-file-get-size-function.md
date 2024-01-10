---
title: MPI_File_get_size function
TOCTitle: MPI_File_get_size function
ms:assetid: f6f80e03-8aee-4a61-80cd-4238e6e80994
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473319(v=VS.85)
ms:contentKeyID: 59360865
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_GET_SIZE
- mpif/MPI_File_get_size
- mpi/MPI_FILE_GET_SIZE
dev_langs:
- C++
- C
description: Learn how to use the MPI_File_get_size function on Microsoft's platform. Understand syntax, parameters, return values, and requirements.
---

# MPI\_File\_get\_size function

Returns the file size.

## Syntax

``` c++
int MPIAPI MPI_File_get_size(
        MPI_File   file,
  _Out_ MPI_Offset *size
);
```

## Parameters

  - *file*  
    File handle.

  - *size* \[out\]  
    Size of the file in bytes.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_GET_SIZE(FH, SIZE, IERROR)
        INTEGER FH, IERROR
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

