---
title: MPI_Win_wait function
TOCTitle: MPI_Win_wait function
ms:assetid: 333bc1f0-460f-42bb-bdeb-c8a1bf40a185
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520617(v=VS.85)
ms:contentKeyID: 59361088
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_WAIT
- mpif/MPI_Win_wait
- mpi/MPI_WIN_WAIT
dev_langs:
- C++
- C
---

# MPI\_Win\_wait function

Completes an RMA exposure epoch begun with [**MPI\_Win\_post**](mpi-win-post-function.md).

## Syntax

``` c++
int MPIAPI MPI_Win_wait(
   MPI_Win win
);
```

## Parameters

  - *win*  
    Window object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_WIN_WAIT(WIN, IERROR)
        INTEGER WIN, IERROR

## Remarks

Completes an RMA exposure epoch started by a call to [**MPI\_Win\_post**](mpi-win-post-function.md) on win. This call matches calls to [**MPI\_Win\_complete**](mpi-win-complete-function.md) issued by each of the origin processes that were granted access to the window during this epoch. The call to [**MPI\_Win\_wait**](mpi-win-wait-function.md) will block until all matching calls to [**MPI\_Win\_complete**](mpi-win-complete-function.md) have occurred. This guarantees that all these origin processes have completed their RMA accesses to the local window. When the call returns, all these RMA accesses will have completed at the target window.

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

