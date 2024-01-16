---
title: MPI_File_set_atomicity function
TOCTitle: MPI_File_set_atomicity function
ms:assetid: f53af688-ddd0-4eb0-a83a-2d31b01d05d1
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473354(v=VS.85)
ms:contentKeyID: 59360890
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_SET_ATOMICITY
- mpif/MPI_File_set_atomicity
- mpi/MPI_FILE_SET_ATOMICITY
dev_langs:
- C++
- C
description: Learn how to set the atomicity mode using MPI_File_set_atomicity function on Microsoft's platform. Includes syntax, parameters, and return values.
---

# MPI\_File\_set\_atomicity function

Sets the atomicity mode.

## Syntax

``` c++
int MPIAPI MPI_File_set_atomicity(
   MPI_File file,
   int      flag
);
```

## Parameters

  - *file*  
    File handle.

  - *flag*  
    True to set atomic mode, false to set nonatomic mode.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_SET_ATOMICITY(FH, FLAG, IERROR)
        INTEGER FH, IERROR
        LOGICAL FLAG
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

