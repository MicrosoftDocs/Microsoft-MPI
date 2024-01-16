---
title: MPI_File_write_ordered_begin function
TOCTitle: MPI_File_write_ordered_begin function
ms:assetid: b51bd73e-3055-4f00-a9f5-27f77b3e8702
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473369(v=VS.85)
ms:contentKeyID: 59360905
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_WRITE_ORDERED_BEGIN
- mpif/MPI_File_write_ordered_begin
- mpi/MPI_FILE_WRITE_ORDERED_BEGIN
dev_langs:
- C++
- C
description: Learn how to use the MPI_File_write_ordered_begin function for split collective writes with shared file pointers on Microsoft's official site.
---

# MPI\_File\_write\_ordered\_begin function

Begins a split collective write using shared file pointer.

## Syntax

``` c++
int MPIAPI MPI_File_write_ordered_begin(
       MPI_File     file,
  _In_ void         *buf,
       int          count,
       MPI_Datatype datatype
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

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_WRITE_ORDERED_BEGIN(FH, BUF, COUNT, DATATYPE, IERROR)
        <type> BUF(*)
        INTEGER FH, COUNT, DATATYPE, IERROR
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

