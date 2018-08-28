---
title: MPI_File_get_info function
TOCTitle: MPI_File_get_info function
ms:assetid: d63b62f7-e4ac-41cf-b19c-5a81a8eaf571
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473316(v=VS.85)
ms:contentKeyID: 59360862
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_GET_INFO
- mpif/MPI_File_get_info
- mpi/MPI_FILE_GET_INFO
dev_langs:
- C++
- C
---

# MPI\_File\_get\_info function

TBD

## Syntax

``` c++
int MPIAPI MPI_File_get_info(
        MPI_File file,
  _Out_ MPI_Info *info
);
```

## Parameters

  - *file*  
    TBD

  - *info* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_FILE_GET_INFO(FH, INFO_USED, IERROR)
        INTEGER FH, INFO_USED, IERROR

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

