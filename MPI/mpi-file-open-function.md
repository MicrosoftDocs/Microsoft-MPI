---
title: MPI_File_open function
TOCTitle: MPI_File_open function
ms:assetid: d3838a60-de06-4dfb-a8dd-4ea0e00fdddc
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473328(v=VS.85)
ms:contentKeyID: 59360874
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_OPEN
- mpif/MPI_File_open
- mpi/MPI_FILE_OPEN
dev_langs:
- C++
- C
---

# MPI\_File\_open function

Opens a file.

## Syntax

``` c++
int MPIAPI MPI_File_open(
        MPI_Comm comm,
  _In_  char     *filename,
        int      amode,
        MPI_Info info,
  _Out_ MPI_File *newfile
);
```

## Parameters

  - *comm*  
    Communicator.

  - *filename* \[in\]  
    Name of file to open.

  - *amode*  
    File access mode.

  - *info*  
    Info object.

  - *newfile* \[out\]  
    File handle.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_OPEN(COMM, FILENAME, AMODE, INFO, FH, IERROR)
        CHARACTER*(*) FILENAME
        INTEGER COMM, AMODE, INFO, FH, IERROR
```

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

