---
title: MPI_Buffer_attach function
TOCTitle: MPI_Buffer_attach function
ms:assetid: 30D28DF2-2734-4BEF-B6EA-66FD40B42EE6
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473240(v=VS.85)
ms:contentKeyID: 59360786
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_BUFFER_ATTACH
- mpif/MPI_Buffer_attach
- mpi/MPI_BUFFER_ATTACH
dev_langs:
- C++
- C
---

# MPI\_Buffer\_attach function

Attaches a user-provided buffer for sending

## Syntax

``` c++
int
MPIAPI MPI_Buffer_attach(
  _In_ void *buffer,
       int  size
);
```

## Parameters

  - *buffer* \[in\]  
    Initial buffer address.

  - *size*  
    Buffer size in bytes.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_BUFFER_ATTACH(BUFFER, SIZE, IERROR)
        <type> BUFFER(*)
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

