---
title: MPI_File_read_at_all function
TOCTitle: MPI_File_read_at_all function
ms:assetid: e2e28f4d-f6b3-49ed-881d-df0834a50a13
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473345(v=VS.85)
ms:contentKeyID: 59360881
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_READ_AT_ALL
- mpif/MPI_File_read_at_all
- mpi/MPI_FILE_READ_AT_ALL
dev_langs:
- C++
- C
description: Master the MPI_File_read_at_all function with our comprehensive guide. Learn syntax, parameters, return values, and requirements for successful implementation.
---

# MPI\_File\_read\_at\_all function

Collective read using explict offset.

## Syntax

``` c++
int MPIAPI MPI_File_read_at_all(
        MPI_File     file,
        MPI_Offset   offset,
  _Out_ void         *buf,
        int          count,
        MPI_Datatype datatype,
  _Out_ MPI_Status   *status
);
```

## Parameters

  - *file*  
    File handle.

  - *offset*  
    File offset.

  - *buf* \[out\]  
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

``` FORTRAN
    MPI_FILE_READ_AT_ALL(FH, OFFSET, BUF, COUNT, DATATYPE, STATUS, IERROR)
        <type> BUF(*)
        INTEGER FH, COUNT, DATATYPE, STATUS(MPI_STATUS_SIZE), IERROR
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

