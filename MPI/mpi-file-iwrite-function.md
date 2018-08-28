---
title: MPI_File_iwrite function
TOCTitle: MPI_File_iwrite function
ms:assetid: 1f2c71dd-8f06-4a96-bb54-449c9bcdcfa1
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473325(v=VS.85)
ms:contentKeyID: 59360871
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_IWRITE
- mpif/MPI_File_iwrite
- mpi/MPI_FILE_IWRITE
dev_langs:
- C++
- C
---

# MPI\_File\_iwrite function

TBD

## Syntax

``` c++
int MPIAPI MPI_File_iwrite(
        MPI_File     file,
  _In_  void         *buf,
        int          count,
        MPI_Datatype datatype,
  _Out_ MPI_Request  *request
);
```

## Parameters

  - *file*  
    TBD

  - *buf* \[in\]  
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

    MPI_FILE_IWRITE(FH, BUF, COUNT, DATATYPE, REQUEST, IERROR)
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

