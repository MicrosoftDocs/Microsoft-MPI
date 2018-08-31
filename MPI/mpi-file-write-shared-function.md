﻿---
title: MPI_File_write_shared function
TOCTitle: MPI_File_write_shared function
ms:assetid: acd56c90-42a4-4e36-8efc-df9e2bc92df9
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473371(v=VS.85)
ms:contentKeyID: 59360907
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_WRITE_ORDERED
- mpi/MPI_FILE_WRITE_ORDERED
- mpi/MPI_File_write_shared
- MPI_File_write_shared
- mpif/MPI_FILE_WRITE_ORDERED
- mpif/MPI_File_write_shared
dev_langs:
- C++
- C
---

# MPI\_File\_write\_shared function

Write using shared file pointer.

## Syntax

``` c++
int MPIAPI MPI_File_write_shared(
        MPI_File     file,
  _In_  void         *buf,
        int          count,
        MPI_Datatype datatype,
  _Out_ MPI_Status   *status
);
```

## Parameters

  - *file*  
    File handle.

  - *buf* \[in\]  
    Initial address of buffer.

  - *count*  
    Number of elements in buffer.

  - *datatype*  
    Datatype of each buffer element.

  - *status* \[out\]  
    Status object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_FILE_WRITE_ORDERED(FH, BUF, COUNT, DATATYPE, STATUS, IERROR)
        <type> BUF(*)
        INTEGER FH, COUNT, DATATYPE, STATUS(MPI_STATUS_SIZE), IERROR

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

