---
title: MPI_File_call_errhandler function
TOCTitle: MPI_File_call_errhandler function
ms:assetid: 9a05a4b8-ee76-4c16-b5c6-57b744a383c3
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473304(v=VS.85)
ms:contentKeyID: 59360850
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_FILE_CALL_ERRHANDLER
- MPI_FILE_CALL_ERRHANDLER
- mpif/MPI_File_call_errhandler
dev_langs:
- C++
- C
---

# MPI\_File\_call\_errhandler function

Calls the error handler installed on a file.

## Syntax

``` c++
int MPIAPI MPI_File_call_errhandler(
   MPI_File file,
   int      errorcode
);
```

## Parameters

  - *file*  
    MPI file with error handler.

  - *errorcode*  
    Error code.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_FILE_CALL_ERRHANDLER(FH, ERRORCODE, IERROR)
        INTEGER FH, ERRORCODE, IERROR

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

