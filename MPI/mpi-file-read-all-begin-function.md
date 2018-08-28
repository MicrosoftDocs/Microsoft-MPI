---
title: MPI_File_read_all_begin function
TOCTitle: MPI_File_read_all_begin function
ms:assetid: ef689025-f05a-4b08-926f-d60d92d653e6
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473342(v=VS.85)
ms:contentKeyID: 59360878
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_READ_ALL_BEGIN
- mpif/MPI_File_read_all_begin
- mpi/MPI_FILE_READ_ALL_BEGIN
dev_langs:
- C++
- C
---

# MPI\_File\_read\_all\_begin function

TBD

## Syntax

``` c++
int MPIAPI MPI_File_read_all_begin(
        MPI_File     file,
  _Out_ void         *buf,
        int          count,
        MPI_Datatype datatype
);
```

## Parameters

  - *file*  
    TBD

  - *buf* \[out\]  
    TBD

  - *count*  
    TBD

  - *datatype*  
    TBD

## Return value

TBD

## Fortran

    MPI_FILE_READ_ALL_BEGIN(FH, BUF, COUNT, DATATYPE, IERROR)
        <type> BUF(*)
        INTEGER FH, COUNT, DATATYPE, IERROR

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

