---
title: MPI_Buffer_detach function
TOCTitle: MPI_Buffer_detach function
ms:assetid: A7F774CA-CE48-401A-92B5-2890951D4CC9
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473241(v=VS.85)
ms:contentKeyID: 59360787
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_BUFFER_DETACH
- mpif/MPI_Buffer_detach
- mpi/MPI_BUFFER_DETACH
dev_langs:
- C++
- C
---

# MPI\_Buffer\_detach function

Removes an existing buffer.

## Syntax

``` c++
int
MPIAPI MPI_Buffer_detach(
  _Out_ void *buffer_addr,
  _Out_ int  *size
);
```

## Parameters

  - *buffer\_addr* \[out\]  
    Initial buffer address.

  - *size* \[out\]  
    Buffer size in bytes.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_BUFFER_DETACH(BUFFER_ADDR, SIZE, IERROR)
        <type> BUFFER_ADDR(*)
        INTEGER SIZE, IERROR

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

