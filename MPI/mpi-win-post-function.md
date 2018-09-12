---
title: MPI_Win_post function
TOCTitle: MPI_Win_post function
ms:assetid: 7bc39c36-ca44-455b-9232-288036278612
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520610(v=VS.85)
ms:contentKeyID: 59361081
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_POST
- mpif/MPI_Win_post
- mpi/MPI_WIN_POST
dev_langs:
- C++
- C
---

# MPI\_Win\_post function

Starts an RMA exposure epoch.

## Syntax

``` c++
int MPIAPI MPI_Win_post(
   MPI_Group group,
   int       assert,
   MPI_Win   win
);
```

## Parameters

  - *group*  
    Group of origin processes.

  - *assert*  
    Used to optimize this call; zero may be used as a default.

  - *win*  
    Window object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_POST(GROUP, ASSERT, WIN, IERROR)
        INTEGER GROUP, ASSERT, WIN, IERROR
```

## Remarks

The *assert* argument is used to indicate special conditions for the post that an implementation may use to optimize the [**MPI\_Win\_post**](mpi-win-post-function.md) operation.  The value zero is always correct.  Other assertion values may be **OR**ed together.  Assertions that are valid for [**MPI\_Win\_post**](mpi-win-post-function.md) are:

- **MPI\_MODE\_NOCHECK** - the matching calls to [**MPI\_Win\_start**](mpi-win-start-function.md) have not yet occurred on any origin processes when the call to [**MPI\_Win\_post**](mpi-win-post-function.md) is made. The nocheck option can be specified by a post call if and only if it is specified by each matching start call.
- **MPI\_MODE\_NOSTORE** - the local window was not updated by local stores (or local get or receive calls) since last synchronization. This may avoid the need for cache synchronization at the post call.
- **MPI\_MODE\_NOPUT** - the local window will not be updated by put or accumulate calls after the post call, until the ensuing (wait) synchronization. This may avoid the need for cache synchronization at the wait call.

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

