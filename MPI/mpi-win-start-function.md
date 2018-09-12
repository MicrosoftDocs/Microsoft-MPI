---
title: MPI_Win_start function
TOCTitle: MPI_Win_start function
ms:assetid: bf2616c8-c541-4f96-a0ae-2ab2401231b9
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520614(v=VS.85)
ms:contentKeyID: 59361085
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_START
- mpif/MPI_Win_start
- mpi/MPI_WIN_START
dev_langs:
- C++
- C
---

# MPI\_Win\_start function

Starts an RMA access epoch for MPI window.

## Syntax

``` c++
int MPIAPI MPI_Win_start(
   MPI_Group group,
   int       assert,
   MPI_Win   win
);
```

## Parameters

  - *group*  
    Group of target processes.

  - *assert*  
    Used to optimize this call; zero may be used as a default.

  - *win*  
    Window object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_START(GROUP, ASSERT, WIN, IERROR)
        INTEGER GROUP, ASSERT, WIN, IERROR
```

## Remarks

The *assert* argument is used to indicate special conditions for the fence that an implementation may use to optimize the [**MPI\_Win\_start**](mpi-win-start-function.md) operation.  The value zero is always correct.  Other assertion values may be or''ed together.  Assertions tha are valid for [**MPI\_Win\_start**](mpi-win-start-function.md) are:

- MPI_MODE_NOCHECK - the matching calls to [**MPI\_Win\_post**](mpi-win-post-function.md) have already completed on all target processes when the call to [**MPI\_Win\_start**](mpi-win-start-function.md) is made. The nocheck option can be specified in a start call if and only if it is specified in each matching post call. This is similar to the optimization of ready-send that may save a handshake when the handshake is implicit in the code. (However, ready-send is matched by a regular receive, whereas both start and post must specify the nocheck option.)


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

