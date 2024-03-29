---
title: MPI_File_write_at_all_begin function
TOCTitle: MPI_File_write_at_all_begin function
ms:assetid: 9b7fcc2e-8b01-4d3a-9055-1e5d6efcf051
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473366(v=VS.85)
ms:contentKeyID: 59360902
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_WRITE_AT_ALL_BEGIN
- mpif/MPI_File_write_at_all_begin
- mpi/MPI_FILE_WRITE_AT_ALL_BEGIN
dev_langs:
- C++
- C
description: Learn about the MPI_File_write_at_all_begin function on Microsoft's official site. Understand its syntax, parameters, return values, and requirements.
---

# MPI\_File\_write\_at\_all\_begin function

Begins a split collective write using explict offset.

## Syntax

``` c++
int MPIAPI MPI_File_write_at_all_begin(
       MPI_File     file,
       MPI_Offset   offset,
  _In_ void         *buf,
       int          count,
       MPI_Datatype datatype
);
```

## Parameters

  - *file*  
    File handle.

  - *offset*  
    File offset.

  - *buf* \[in\]  
    Initial address of buffer.

  - *count*  
    Number of elements in buffer.

  - *datatype*  
    Datatype of each buffer element.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_WRITE_AT_ALL_BEGIN(FH, OFFSET, BUF, COUNT, DATATYPE, IERROR)
        <type> BUF(*)
        INTEGER FH, COUNT, DATATYPE, IERROR
        INTEGER(KIND=MPI_OFFSET_KIND) OFFSET
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

