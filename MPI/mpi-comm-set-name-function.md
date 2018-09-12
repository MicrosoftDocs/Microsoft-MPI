﻿---
title: MPI_Comm_set_name function
TOCTitle: MPI_Comm_set_name function
ms:assetid: 514ae37f-893b-46ed-9cf5-a2308b7a93cf
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473282(v=VS.85)
ms:contentKeyID: 59360828
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_SET_NAME
- mpif/MPI_Comm_set_name
- mpi/MPI_COMM_SET_NAME
dev_langs:
- C++
- C
---

# MPI\_Comm\_set\_name function

Sets the print name for a communicator.

## Syntax

``` c++
int MPIAPI MPI_Comm_set_name(
   MPI_Comm    comm,
   _In_z_ char *comm_name
);
```

## Parameters

  - *comm*  
    Communicator to name.

  - *comm\_name*  
    Name for communicator.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMM_SET_NAME(COMM, COMM_NAME, IERROR)
        INTEGER COMM, IERROR
        CHARACTER*(*) COMM_NAME
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

[MPI Miscellaneous Functions](mpi-miscellaneous-functions.md)

