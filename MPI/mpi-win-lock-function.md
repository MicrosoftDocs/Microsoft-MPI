---
title: MPI_Win_lock function
TOCTitle: MPI_Win_lock function
ms:assetid: e5bd3a8b-264f-4156-958f-e325db1c129c
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520609(v=VS.85)
ms:contentKeyID: 59361080
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_LOCK
- mpif/MPI_Win_lock
- mpi/MPI_WIN_LOCK
dev_langs:
- C++
- C
---

# MPI\_Win\_lock function

Begins an RMA access epoch at the target process.

## Syntax

``` c++
int MPIAPI MPI_Win_lock(
   int     lock_type,
   int     rank,
   int     assert,
   MPI_Win win
);
```

## Parameters

  - *lock\_type*  
    Indicates whether other processes may access the target window at the same time (if **MPI\_LOCK\_SHARED**) or not (**MPI\_LOCK\_EXCLUSIVE**).

  - *rank*  
    Rank of locked window.

  - *assert*  
    Used to optimize this call; zero may be used as a default.

  - *win*  
    Window object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_WIN_LOCK(LOCK_TYPE, RANK, ASSERT, WIN, IERROR)
        INTEGER LOCK_TYPE, RANK, ASSERT, WIN, IERROR

## Remarks

The name of this routine is misleading.  In particular, this routine need not block, except when the target process is the calling process.

Implementations may restrict the use of RMA communication that is synchronized by lock calls to windows in memory allocated by [**MPI\_Alloc\_mem**](mpi-alloc-mem-function.md). Locks can be used portably only in such memory.

The *assert* argument is used to indicate special conditions for the fence that an implementation may use to optimize the [**MPI\_Win\_fence**](mpi-win-fence-function.md) operation.  The value zero is always correct.  Other assertion values may be **OR**ed together.  Assertions that are valid for [**MPI\_Win\_fence**](mpi-win-fence-function.md) are:

- **MPI\_MODE\_NOCHECK** - no other process holds, or will attempt to acquire a conflicting lock, while the caller holds the window lock. This is useful when mutual exclusion is achieved by other means, but the coherence operations that may be attached to the lock and unlock calls are still required.


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

