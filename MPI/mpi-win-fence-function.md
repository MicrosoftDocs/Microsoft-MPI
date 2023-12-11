---
title: MPI_Win_fence function
TOCTitle: MPI_Win_fence function
ms:assetid: 330ac361-b77d-4047-ace9-e6581700bb4c
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520602(v=VS.85)
ms:contentKeyID: 59361073
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_FENCE
- mpif/MPI_Win_fence
- mpi/MPI_WIN_FENCE
dev_langs:
- C++
- C
description: Master MPI_Win_fence function with our comprehensive guide. Learn about its syntax, parameters, return values, and special conditions for optimization.
---

# MPI\_Win\_fence function

Performs an MPI fence synchronization on an MPI window.

## Syntax

``` c++
int MPIAPI MPI_Win_fence(
   int     assert,
   MPI_Win win
);
```

## Parameters

  - *assert*  
    Program assertion.

  - *win*  
    Window object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_FENCE(ASSERT, WIN, IERROR)
        INTEGER ASSERT, WIN, IERROR
```

## Remarks

The *assert* argument is used to indicate special conditions for the fence that an implementation may use to optimize the [**MPI\_Win\_fence**](mpi-win-fence-function.md) operation.  The value zero is always correct.  Other assertion values may be **OR**ed together.  Assertions that are valid for [**MPI\_Win\_fence**](mpi-win-fence-function.md) are:

- **MPI\_MODE\_NOSTORE** - the local window was not updated by local stores (or local get or receive calls) since last synchronization.
- **MPI\_MODE\_NOPUT** - the local window will not be updated by put or accumulate calls after the fence call, until the ensuing (fence) synchronization.
- **MPI\_MODE\_NOPRECEDE** - the fence does not complete any sequence of locally issued RMA calls. If this assertion is given by any process in the window group, then it must be given by all processes in the group.
- **MPI\_MODE\_NOSUCCEED** - the fence does not start any sequence of locally issued RMA calls. If the assertion is given by any process in the window group, then it must be given by all processes in the group.

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

[MPI One-Sided Communications Functions](mpi-one-sided-communications-functions.md)

