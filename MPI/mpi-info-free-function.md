---
title: MPI_Info_free function
TOCTitle: MPI_Info_free function
ms:assetid: 2ecb355c-9739-4d20-8cb5-ef17a1c3c156
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473412(v=VS.85)
ms:contentKeyID: 59360948
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_INFO_FREE
- mpif/MPI_Info_free
- mpi/MPI_INFO_FREE
dev_langs:
- C++
- C
---

# MPI\_Info\_free function

Frees an info object.

## Syntax

``` c++
int MPIAPI MPI_Info_free(
  _Inout_ MPI_Info *info
);
```

## Parameters

  - *info* \[in, out\]  
    Info object to be freed.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_INFO_FREE(INFO, IERROR)
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

[MPI Info Object Functions](mpi-info-object-functions.md)

