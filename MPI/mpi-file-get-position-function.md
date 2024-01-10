---
title: MPI_File_get_position function
TOCTitle: MPI_File_get_position function
ms:assetid: da6ead7e-c626-4a1d-a3b3-036907cff725
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473317(v=VS.85)
ms:contentKeyID: 59360863
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_GET_POSITION
- mpif/MPI_File_get_position
- mpi/MPI_FILE_GET_POSITION
dev_langs:
- C++
- C
---

# MPI\_File\_get\_position function

Returns the current position of the individual file pointer in etype units relative to the current view.

## Syntax

``` c++
int MPIAPI MPI_File_get_position(
        MPI_File   file,
  _Out_ MPI_Offset *offset
);
```

## Parameters

  - *file*  
    File handle.

  - *offset* \[out\]  
    Offset of individual file pointer.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_GET_POSITION(FH, OFFSET, IERROR)
        INTEGER FH, IERROR
        INTEGER(KIND=MPI_OFFSET_KIND) OFFSET
```

## Requirements

<table>
<colgroup>
<col  />
<col  />
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

