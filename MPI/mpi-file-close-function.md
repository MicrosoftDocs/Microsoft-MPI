---
title: MPI_File_close function
TOCTitle: MPI_File_close function
ms:assetid: 8cd5bcba-0edd-462c-80ae-474929eafa0a
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473305(v=VS.85)
ms:contentKeyID: 59360851
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_CLOSE
- mpif/MPI_File_close
- mpi/MPI_FILE_CLOSE
dev_langs:
- C++
- C
---

# MPI\_File\_close function

Closes a file.

## Syntax

``` c++
int MPIAPI MPI_File_close(
  _In_ MPI_File *file
);
```

## Parameters

  - *file* \[in\]  
    File handle.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_CLOSE(FH, IERROR)
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

