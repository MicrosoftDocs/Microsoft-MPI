---
title: MPI_File_get_errhandler function
TOCTitle: MPI_File_get_errhandler function
ms:assetid: 70271a98-d725-476a-a068-28ad5e5b420f
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473314(v=VS.85)
ms:contentKeyID: 59360860
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_GET_ERRHANDLER
- mpif/MPI_File_get_errhandler
- mpi/MPI_FILE_GET_ERRHANDLER
dev_langs:
- C++
- C
---

# MPI\_File\_get\_errhandler function

Gets the error handler attached to a file.

## Syntax

``` c++
int MPIAPI MPI_File_get_errhandler(
        MPI_File       file,
  _Out_ MPI_Errhandler *errhandler
);
```

## Parameters

  - *file*  
    MPI file.

  - *errhandler* \[out\]  
    Handler currently associated with file.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_GET_ERRHANDLER(FILE, ERRHANDLER, IERROR)
        INTEGER FILE, ERRHANDLER, IERROR
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

[MPI Management Functions](mpi-management-functions.md)

