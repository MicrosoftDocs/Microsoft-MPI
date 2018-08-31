---
title: MPI_File_set_errhandler function
TOCTitle: MPI_File_set_errhandler function
ms:assetid: 32f30a82-85ec-434a-b52f-ebfe563394ec
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473355(v=VS.85)
ms:contentKeyID: 59360891
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_SET_ERRHANDLER
- mpif/MPI_File_set_errhandler
- mpi/MPI_FILE_SET_ERRHANDLER
dev_langs:
- C++
- C
---

# MPI\_File\_set\_errhandler function

Sets the error handler for an MPI file.

## Syntax

``` c++
int MPIAPI MPI_File_set_errhandler(
   MPI_File       file,
   MPI_Errhandler errhandler
);
```

## Parameters

  - *file*  
    MPI file.

  - *errhandler*  
    New error handler for file.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_FILE_SET_ERRHANDLER(FILE, ERRHANDLER, IERROR)
        INTEGER FILE, ERRHANDLER, IERROR

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

[MPI Management Functions](mpi-management-functions.md)

