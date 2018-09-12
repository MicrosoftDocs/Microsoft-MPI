---
title: MPI_Info_get_valuelen function
TOCTitle: MPI_Info_get_valuelen function
ms:assetid: b6538c37-3671-4ad0-89d3-db824c918b67
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473416(v=VS.85)
ms:contentKeyID: 59360952
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_INFO_GET_VALUELEN
- mpif/MPI_Info_get_valuelen
- mpi/MPI_INFO_GET_VALUELEN
dev_langs:
- C++
- C
---

# MPI\_Info\_get\_valuelen function

Retrieves the length of the value associated with a key.

## Syntax

``` c++
int MPIAPI MPI_Info_get_valuelen(
        MPI_Info info,
  _In_  char     *key,
  _Out_ int      *valuelen,
  _Out_ int      *flag
);
```

## Parameters

  - *info*  
    Info object.

  - *key* \[in\]  
    Key.

  - *valuelen* \[out\]  
    Length of value argument.

  - *flag* \[out\]  
    True if key defined, false if not.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_INFO_GET_VALUELEN(INFO, KEY, VALUELEN, FLAG, IERROR)
        INTEGER INFO, VALUELEN, IERROR
        LOGICAL FLAG
        CHARACTER*(*) KEY
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

[MPI Info Object Functions](mpi-info-object-functions.md)

