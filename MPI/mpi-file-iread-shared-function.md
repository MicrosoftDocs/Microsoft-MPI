﻿---
title: MPI_File_iread_shared function
TOCTitle: MPI_File_iread_shared function
ms:assetid: b88323d5-1b58-4428-8d8a-61a40b7b030a
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473324(v=VS.85)
ms:contentKeyID: 59360870
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_IREAD_SHARED
- mpif/MPI_File_iread_shared
- mpi/MPI_FILE_IREAD_SHARED
dev_langs:
- C++
- C
---

# MPI\_File\_iread\_shared function

Nonblocking read using shared file pointer.

## Syntax

``` c++
int MPIAPI MPI_File_iread_shared(
        MPI_File     file,
  _Out_ void         *buf,
        int          count,
        MPI_Datatype datatype,
  _Out_ MPI_Request  *request
);
```

## Parameters

  - *file*  
    File handle.

  - *buf* \[out\]  
    Initial address of buffer.

  - *count*  
    Number of elements in buffer.

  - *datatype*  
    Datatype of each buffer element.

  - *request* \[out\]  
    Request object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_IREAD_SHARED(FH, BUF, COUNT, DATATYPE, REQUEST, IERROR)
        <type> BUF(*)
        INTEGER FH, COUNT, DATATYPE, REQUEST, IERROR
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

