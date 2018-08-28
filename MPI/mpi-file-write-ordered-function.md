---
title: MPI_File_write_ordered function
TOCTitle: MPI_File_write_ordered function
ms:assetid: df40b0a9-4d75-423f-a527-a31541a29c20
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473368(v=VS.85)
ms:contentKeyID: 59360904
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_WRITE_ORDERED
- mpif/MPI_File_write_ordered
- mpi/MPI_FILE_WRITE_ORDERED
dev_langs:
- C++
- C
---

# MPI\_File\_write\_ordered function

TBD

## Syntax

``` c++
int MPIAPI MPI_File_write_ordered(
  _In_  MPI_File     file,
  _In_  void         *buf,
        int          count,
        MPI_Datatype datatype,
  _Out_ MPI_Status   *status
);
```

## Parameters

  - *file* \[in\]  
    TBD

  - *buf* \[in\]  
    TBD

  - *count*  
    TBD

  - *datatype*  
    TBD

  - *status* \[out\]  
    TBD

## Return value

TBD

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

