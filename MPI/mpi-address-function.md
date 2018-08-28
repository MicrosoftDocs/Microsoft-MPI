---
title: MPI_Address function
TOCTitle: MPI_Address function
ms:assetid: 068bd9d3-206d-4246-9b6f-144a1fcdbf26
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn502496(v=VS.85)
ms:contentKeyID: 59360768
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ADDRESS
- mpif/MPI_Address
- mpi/MPI_ADDRESS
dev_langs:
- C++
- C
---

# MPI\_Address function

This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Get\_address**](mpi-get-address-function.md) function.

## Syntax

``` c++
int
MPIAPI MPI_Address(
  _In_  void     *location,
  _Out_ MPI_Aint *address
);
```

## Parameters

  - *location* \[in\]  
    TBD

  - *address* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_ADDRESS(LOCATION, ADDRESS, IERROR)
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

[MPI Miscellaneous Functions](mpi-miscellaneous-functions.md)

[**MPI\_Get\_address**](mpi-get-address-function.md)

