---
title: MPI_Win_create function
TOCTitle: MPI_Win_create function
ms:assetid: fccf3c21-8840-4de4-8d97-e8bb778771e2
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520596(v=VS.85)
ms:contentKeyID: 59361067
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_CREATE
- mpif/MPI_Win_create
- mpi/MPI_WIN_CREATE
dev_langs:
- C++
- C
description: Learn about MPI_Win_create function for one-sided communication on Microsoft's official site. Understand syntax, parameters, and return values.
---

# MPI\_Win\_create function

Creates an MPI Window object for one-sided communication.

## Syntax

``` c++
int MPIAPI MPI_Win_create(
  _In_  void     *base,
        MPI_Aint size,
        int      disp_unit,
        MPI_Info info,
        MPI_Comm comm,
  _Out_ MPI_Win  *win
);
```

## Parameters

  - *base* \[in\]  
    Initial address of the memory window.

  - *size*  
    Size of the memory window in bytes.

  - *disp\_unit*  
    Local unit size for displacements, in bytes.

  - *info*  
    Info argument.

  - *comm*  
    Communicator.

  - *win* \[out\]  
    Window object returned by the call.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_CREATE(BASE, SIZE, DISP_UNIT, INFO, COMM, WIN, IERROR)
        <type> BASE(*)
        INTEGER(KIND=MPI_ADDRESS_KIND) SIZE
        INTEGER DISP_UNIT, INFO, COMM, WIN, IERROR
```

## Remarks

The call is collective on an intracommunicator. [**MPI\_Win\_create**](mpi-win-create-function.md) allows each process to specify a window in its memory that is made accessible to accesses by remote processes. The call returns an opaque object that represents the group of processes that own and access the set of windows, and the attributes of each window, as specified by the initialization call.

## Requirements

<table>
<colgroup>
<col/>
<col/>
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

[MPI One-Sided Communications Functions](mpi-one-sided-communications-functions.md)

