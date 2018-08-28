---
title: MPI_File_get_amode function
TOCTitle: MPI_File_get_amode function
ms:assetid: a100cb7d-34a9-4f53-9c6e-9f0c4bbc8f09
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473311(v=VS.85)
ms:contentKeyID: 59360857
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_GET_AMODE
- mpif/MPI_File_get_amode
- mpi/MPI_FILE_GET_AMODE
dev_langs:
- C++
- C
---

# MPI\_File\_get\_amode function

TBD

## Syntax

``` c++
int MPIAPI MPI_File_get_amode(
        MPI_File file,
  _Out_ int      *amode
);
```

## Parameters

  - *file*  
    TBD

  - *amode* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_FILE_GET_AMODE(FH, AMODE, IERROR)
        INTEGER FH, AMODE, IERROR

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

