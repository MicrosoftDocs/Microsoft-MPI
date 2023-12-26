---
title: MPI_File_get_position_shared function
TOCTitle: MPI_File_get_position_shared function
ms:assetid: dc3cb8ad-032d-49b4-a9fc-97ae738aef4e
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473318(v=VS.85)
ms:contentKeyID: 59360864
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_GET_POSITION_SHARED
- mpif/MPI_File_get_position_shared
- mpi/MPI_FILE_GET_POSITION_SHARED
dev_langs:
- C++
- C
description: Learn about the MPI_File_get_position_shared function on Microsoft's site. Understand its syntax, parameters, return value, and requirements.
---

# MPI\_File\_get\_position\_shared function

Returns the current position of the shared file pointer in etype units relative to the current view.

## Syntax

``` c++
int MPIAPI MPI_File_get_position_shared(
        MPI_File   file,
  _Out_ MPI_Offset *offset
);
```

## Parameters

  - *file*  
    File handle.

  - *offset* \[out\]  
    Offset of shared file pointer.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_GET_POSITION_SHARED(FH, OFFSET, IERROR)
        INTEGER FH, IERROR
        INTEGER(KIND=MPI_OFFSET_KIND) OFFSET
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

