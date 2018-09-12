---
title: MPI_Start function
TOCTitle: MPI_Start function
ms:assetid: 3bb5cee2-1add-4fe5-a73e-61cf1ff0b159
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473473(v=VS.85)
ms:contentKeyID: 59361008
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_START
- mpif/MPI_Start
- mpi/MPI_START
dev_langs:
- C++
- C
---

# MPI\_Start function

Initiates a communication with a persistent request handle.

## Syntax

``` c++
int MPIAPI MPI_Start(
   _Inout_ MPI_Request *request
);
```

## Parameters

  - *request*  
    Communication request.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_START(REQUEST, IERROR)
        INTEGER REQUEST, IERROR
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

[MPI Point to Point Functions](mpi-point-to-point-functions.md)

