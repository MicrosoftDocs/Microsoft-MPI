---
title: MPI_Info_get_nthkey function
TOCTitle: MPI_Info_get_nthkey function
ms:assetid: 6c269257-df91-4101-a042-81bed6f90f7e
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473415(v=VS.85)
ms:contentKeyID: 59360951
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_INFO_GET_NTHKEY
- mpif/MPI_Info_get_nthkey
- mpi/MPI_INFO_GET_NTHKEY
dev_langs:
- C++
- C
description: Explore MPI_Info_get_nthkey function on Microsoft's learning platform. Understand syntax, parameters, return values, and related requirements.
---

# MPI\_Info\_get\_nthkey function

Returns the nth defined key in info object.

## Syntax

``` c++
int MPIAPI MPI_Info_get_nthkey(
   MPI_Info                           info,
   int                                n,
   _Out_z_cap_(MPI_MAX_INFO_KEY) char *key
);
```

## Parameters

  - *info*  
    Info object.

  - *n*  
    Key number.

  - *key*  
    Key. The maximum number of characters is **MPI\_MAX\_INFO\_KEY**.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_INFO_GET_NTHKEY(INFO, N, KEY, IERROR)
        INTEGER INFO, N, IERROR
        CHARACTER*(*) KEY
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

[MPI Info Object Functions](mpi-info-object-functions.md)

