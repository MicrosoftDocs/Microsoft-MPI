---
title: MPI_Info_get function
TOCTitle: MPI_Info_get function
ms:assetid: f7909375-f67e-4339-9cce-7373813ab4bf
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473413(v=VS.85)
ms:contentKeyID: 59360949
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_INFO_GET
- mpif/MPI_Info_get
- mpi/MPI_INFO_GET
dev_langs:
- C++
- C
description: Learn how to use the MPI_Info_get function on Microsoft's official site. Retrieve values associated with keys and handle errors effectively.
---

# MPI\_Info\_get function

Retrieves the value associated with a key.

## Syntax

``` c++
int MPIAPI MPI_Info_get(
        MPI_Info                   info,
  _In_  char                       *key,
        int                        valuelen,
        _Out_z_cap_(valuelen) char *value,
  _Out_ int                        *flag
);
```

## Parameters

  - *info*  
    Info object.

  - *key* \[in\]  
    Key.

  - *valuelen*  
    Length of value argument.

  - *value*  
    Value.

  - *flag* \[out\]  
    True if key defined, false if not.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_INFO_GET(INFO, KEY, VALUELEN, VALUE, FLAG, IERROR)
        INTEGER INFO, VALUELEN, IERROR
        CHARACTER*(*) KEY, VALUE
        LOGICAL FLAG
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

