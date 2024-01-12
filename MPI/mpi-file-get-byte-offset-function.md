---
title: MPI_File_get_byte_offset function
TOCTitle: MPI_File_get_byte_offset function
ms:assetid: 8174a682-6f67-42b9-81eb-c08adb99ca48
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473313(v=VS.85)
ms:contentKeyID: 59360859
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_GET_BYTE_OFFSET
- mpif/MPI_File_get_byte_offset
- mpi/MPI_FILE_GET_BYTE_OFFSET
dev_langs:
- C++
- C
description: Learn how to use the MPI_File_get_byte_offset function on Microsoft's platform. Understand syntax, parameters, return values, and requirements.
---

# MPI\_File\_get\_byte\_offset function

Returns the absolute byte position in the file corresponding to "offset" etypes relative to the current view.

## Syntax

``` c++
int MPIAPI MPI_File_get_byte_offset(
        MPI_File   file,
        MPI_Offset offset,
  _Out_ MPI_Offset *disp
);
```

## Parameters

  - *file*  
    File handle.

  - *offset*  
    Offset.

  - *disp* \[out\]  
    Absolute byte position of offset.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_GET_BYTE_OFFSET(FH, OFFSET, DISP, IERROR)
        INTEGER FH, IERROR
        INTEGER(KIND=MPI_OFFSET_KIND) OFFSET, DISP
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

