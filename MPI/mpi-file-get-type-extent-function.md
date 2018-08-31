---
title: MPI_File_get_type_extent function
TOCTitle: MPI_File_get_type_extent function
ms:assetid: 717f88ab-b3fe-46c4-ad79-277726dae8a3
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473320(v=VS.85)
ms:contentKeyID: 59360866
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_GET_TYPE_EXTENT
- mpif/MPI_File_get_type_extent
- mpi/MPI_FILE_GET_TYPE_EXTENT
dev_langs:
- C++
- C
---

# MPI\_File\_get\_type\_extent function

Returns the extent of datatype in the file.

## Syntax

``` c++
int MPIAPI MPI_File_get_type_extent(
        MPI_File     file,
        MPI_Datatype datatype,
  _Out_ MPI_Aint     *extent
);
```

## Parameters

  - *file*  
    File handle.

  - *datatype*  
    Datatype.

  - *extent* \[out\]  
    Extent of the datatype.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_FILE_GET_TYPE_EXTENT(FH, DATATYPE, EXTENT, IERROR)
        INTEGER FH, DATATYPE, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) EXTENT

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

