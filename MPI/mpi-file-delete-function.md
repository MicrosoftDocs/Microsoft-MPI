---
title: MPI_File_delete function
TOCTitle: MPI_File_delete function
ms:assetid: ecfedbef-e88b-43e7-b48b-11a7ead3f788
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473307(v=VS.85)
ms:contentKeyID: 59360853
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_DELETE
- mpif/MPI_File_delete
- mpi/MPI_FILE_DELETE
dev_langs:
- C++
- C
---

# MPI\_File\_delete function

Deletes a file.

## Syntax

``` c++
int MPIAPI MPI_File_delete(
  _In_ char     *filename,
       MPI_Info info
);
```

## Parameters

  - *filename* \[in\]  
    Name of file to delete.

  - *info*  
    Info object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_DELETE(FILENAME, INFO, IERROR)
        CHARACTER*(*) FILENAME
        INTEGER INFO, IERROR
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

