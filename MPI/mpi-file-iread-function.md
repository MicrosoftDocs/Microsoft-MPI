---
title: MPI_File_iread function
TOCTitle: MPI_File_iread function
ms:assetid: e1f4966f-5c96-494d-9e51-249b124d8fd9
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473322(v=VS.85)
ms:contentKeyID: 59360868
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_IREAD
- mpif/MPI_File_iread
- mpi/MPI_FILE_IREAD
dev_langs:
- C++
- C
---

# MPI\_File\_iread function

TBD

## Syntax

``` c++
int MPIAPI MPI_File_iread(
        MPI_File     file,
  _Out_ void         *buf,
        int          count,
        MPI_Datatype datatype,
  _Out_ MPI_Request  *request
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

  - *request* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_FILE_IREAD(FH, BUF, COUNT, DATATYPE, REQUEST, IERROR)
        <type> BUF(*)
        INTEGER FH, COUNT, DATATYPE, REQUEST, IERROR

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

