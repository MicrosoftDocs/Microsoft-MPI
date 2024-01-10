---
title: MPI_Cartdim_get function
TOCTitle: MPI_Cartdim_get function
ms:assetid: f12febe5-5739-4b77-a741-4011dc7c1ec0
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473244(v=VS.85)
ms:contentKeyID: 59360790
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_CARTDIM_GET
- mpif/MPI_Cartdim_get
- mpi/MPI_CARTDIM_GET
dev_langs:
- C++
- C
---

# MPI\_Cartdim\_get function

Retrieves Cartesian topology information associated with a communicator.

## Syntax

``` c++
int MPIAPI MPI_Cartdim_get(
        MPI_Comm comm,
  _Out_ int      *ndims
);
```

## Parameters

  - *comm*  
    Communicator with cartesian structure.

  - *ndims* \[out\]  
    Number of dimensions of the cartesian structure.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_CARTDIM_GET(COMM, NDIMS, IERROR)
        INTEGER COMM, NDIMS, IERROR
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

[MPI Process Topology Functions](mpi-process-topology-functions.md)

