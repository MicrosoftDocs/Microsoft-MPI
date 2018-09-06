---
title: MPI_Type_get_name function
TOCTitle: MPI_Type_get_name function
ms:assetid: e4c1b64b-2aa4-49be-8268-d139b65cc5ec
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520572(v=VS.85)
ms:contentKeyID: 59361043
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_GET_NAME
- mpif/MPI_Type_get_name
- mpi/MPI_TYPE_GET_NAME
dev_langs:
- C++
- C
---

# MPI\_Type\_get\_name function

Get the print name for a datatype.

## Syntax

``` c++
int MPIAPI MPI_Type_get_name(
        MPI_Datatype                                                type,
        _Out_z_cap_post_count_(MPI_MAX_OBJECT_NAME,*resultlen) char *type_name,
  _Out_ int                                                         *resultlen
);
```

## Parameters

  - *type*  
    Datatype whose name is to be returned.

  - *type\_name*  
    The name previously stored on the datatype, or a empty string if no such name exists.

  - *resultlen* \[out\]  
    Length of returned name.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_TYPE_GET_NAME(DATATYPE, TYPE_NAME, RESULTLEN, IERROR)
        INTEGER DATATYPE, RESULTLEN, IERROR
        CHARACTER*(*) TYPE_NAME

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

[MPI Miscellaneous Functions](mpi-miscellaneous-functions.md)

