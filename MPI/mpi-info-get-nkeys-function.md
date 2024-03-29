---
title: MPI_Info_get_nkeys function
TOCTitle: MPI_Info_get_nkeys function
ms:assetid: a4b7e3c3-24be-494b-987f-970b332b8f94
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473414(v=VS.85)
ms:contentKeyID: 59360950
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_INFO_GET_NKEYS
- mpif/MPI_Info_get_nkeys
- mpi/MPI_INFO_GET_NKEYS
dev_langs:
- C++
- C
description: Learn about the MPI_Info_get_nkeys function on Microsoft's official site. Understand its syntax, parameters, return values, and related requirements.
---

# MPI\_Info\_get\_nkeys function

Returns the number of currently defined keys in info object.

## Syntax

``` c++
int MPIAPI MPI_Info_get_nkeys(
        MPI_Info info,
  _Out_ int      *nkeys
);
```

## Parameters

  - *info*  
    Info object.

  - *nkeys* \[out\]  
    Number of defined keys.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_INFO_GET_NKEYS(INFO, NKEYS, IERROR)
        INTEGER INFO, NKEYS, IERROR
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

