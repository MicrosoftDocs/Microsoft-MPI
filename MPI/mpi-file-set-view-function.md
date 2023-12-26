---
title: MPI_File_set_view function
TOCTitle: MPI_File_set_view function
ms:assetid: 4e09feaf-1242-4ddb-9459-e1047625826e
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473358(v=VS.85)
ms:contentKeyID: 59360894
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_SET_VIEW
- mpif/MPI_File_set_view
- mpirf/MPI_FILE_SET_VIEW
- mpi/MPI_FILE_SET_VIEW
dev_langs:
- C++
- C
description: Learn how to set the file view using MPI_File_set_view function on Microsoft's platform. Includes syntax, parameters, and return values.
---

# MPI\_File\_set\_view function

Sets the file view.

## Syntax

``` c++
int MPIAPI MPI_File_set_view(
       MPI_File     file,
       MPI_Offset   disp,
       MPI_Datatype etype,
       MPI_Datatype filetype,
  _In_ char         *datarep,
       MPI_Info     info
);
```

## Parameters

  - *file*  
    File handle.

  - *disp*  
    Displacement.

  - *etype*  
    Elementary datatype.

  - *filetype*  
    Filetype.

  - *datarep* \[in\]  
    Data representation.

  - *info*  
    Info object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_SET_VIEW(FH, DISP, ETYPE, FILETYPE, DATAREP, INFO, IERROR)
        INTEGER FH, ETYPE, FILETYPE, INFO, IERROR
        CHARACTER*(*) DATAREP
        INTEGER(KIND=MPI_OFFSET_KIND) DISP
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

