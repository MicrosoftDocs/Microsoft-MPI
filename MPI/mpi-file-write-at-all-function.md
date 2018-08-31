---
title: MPI_File_write_at_all function
TOCTitle: MPI_File_write_at_all function
ms:assetid: c75996ae-57c7-42d2-b091-a68420d68f63
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473365(v=VS.85)
ms:contentKeyID: 59360901
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_WRITE_AT_ALL
- mpif/MPI_File_write_at_all
- mpi/MPI_FILE_WRITE_AT_ALL
dev_langs:
- C++
- C
---

# MPI\_File\_write\_at\_all function

Collective write using explict offset.

## Syntax

``` c++
int MPIAPI MPI_File_write_at_all(
        MPI_File     file,
        MPI_Offset   offset,
  _In_  void         *buf,
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

    MPI_FILE_WRITE_AT_ALL(FH, OFFSET, BUF, COUNT, DATATYPE, STATUS, IERROR)
        <type> BUF(*)
        INTEGER FH, COUNT, DATATYPE, STATUS(MPI_STATUS_SIZE), IERROR
        INTEGER(KIND=MPI_OFFSET_KIND) OFFSET

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

