---
title: MPI_File_read_ordered_begin function
TOCTitle: MPI_File_read_ordered_begin function
ms:assetid: d73516a2-1ac2-45e7-9e0a-988ebf388791
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473349(v=VS.85)
ms:contentKeyID: 59360885
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_READ_ORDERED_BEGIN
- mpif/MPI_File_read_ordered_begin
- mpi/MPI_FILE_READ_ORDERED_BEGIN
dev_langs:
- C++
- C
---

# MPI\_File\_read\_ordered\_begin function

Begins a split collective read using shared file pointer.

## Syntax

``` c++
int MPIAPI MPI_File_read_ordered_begin(
        MPI_File     file,
  _Out_ void         *buf,
        int          count,
        MPI_Datatype datatype
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

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_READ_ORDERED_BEGIN(FH, BUF, COUNT, DATATYPE, IERROR)
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

