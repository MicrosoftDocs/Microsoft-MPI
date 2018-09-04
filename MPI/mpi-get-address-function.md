---
title: MPI_Get_address function
TOCTitle: MPI_Get_address function
ms:assetid: 8ecaca8f-2b45-47ea-b329-95ae70fa032f
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473379(v=VS.85)
ms:contentKeyID: 59360915
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GET_ADDRESS
- mpif/MPI_Get_address
- mpi/MPI_GET_ADDRESS
dev_langs:
- C++
- C
---

# MPI\_Get\_address function

Gets the address of a location in memory.

## Syntax

``` c++
int MPIAPI MPI_Get_address(
  _In_  void     *location,
  _Out_ MPI_Aint *address
);
```

## Parameters

  - *location* \[in\]  
    Location in caller memory.

  - *address* \[out\]  
    Address of location.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_GET_ADDRESS(LOCATION, ADDRESS, IERROR)
        <type> LOCATION(*)
        INTEGER IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) ADDRESS

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

[MPI Datatype Functions](mpi-datatype-functions.md)

