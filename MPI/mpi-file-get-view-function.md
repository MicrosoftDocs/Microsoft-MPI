---
title: MPI_File_get_view function
TOCTitle: MPI_File_get_view function
ms:assetid: 5760eaeb-fba1-4a07-9e9c-e9ef83c29d16
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473321(v=VS.85)
ms:contentKeyID: 59360867
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_GET_VIEW
- mpif/MPI_File_get_view
- mpi/MPI_FILE_GET_VIEW
dev_langs:
- C++
- C
---

# MPI\_File\_get\_view function

Returns the file view.

## Syntax

``` c++
int MPIAPI MPI_File_get_view(
        MPI_File                                 file,
  _Out_ MPI_Offset                               *disp,
  _Out_ MPI_Datatype                             *etype,
  _Out_ MPI_Datatype                             *filetype,
        _Out_z_cap_(MPI_MAX_DATAREP_STRING) char *datarep
);
```

## Parameters

  - *file*  
    File handle.

  - *disp* \[out\]  
    Displacement.

  - *etype* \[out\]  
    Elementary datatype.

  - *filetype* \[out\]  
    Filetype.

  - *datarep*  
    Data representation.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_GET_VIEW(FH, DISP, ETYPE, FILETYPE, DATAREP, IERROR)
        INTEGER FH, ETYPE, FILETYPE, IERROR
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

