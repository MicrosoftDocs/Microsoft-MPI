---
title: MPI_Win_create_dynamic function
TOCTitle: MPI_Win_create_dynamic function
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_CREATE_DYNAMIC
- mpif/MPI_Win_create_dynamic
- mpi/MPI_WIN_CREATE_DYNAMIC
dev_langs:
- C++
- C
description: Learn how to use the MPI_Win_create_dynamic function for dynamic memory control in MS-MPI. Detailed syntax, parameters, and return values explained.
---

# MPI\_Win\_create\_dynamic function

Creates a window that allows the user to dynamically control which memory is exposed by the window.

## Syntax

``` c++
int MPIAPI MPI_Win_create_dynamic(
        MPI_Info info,
        MPI_Comm comm,
  _Out_ MPI_Win  *win
);
```

## Parameters

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
    MPI_WIN_CREATE_DYNAMIC(INFO, COMM, WIN, IERROR)
        INTEGER INFO, COMM, WIN, IERROR
```

## Remarks

This is a collective call executed by all processes in the group of *comm*. It returns a window *win* without memory attached. This routine returns a window object that can be used by these processes to perform RMA operations on attached memory. 

The *info* argument can be used to specify hints similar to the info argument for [**MPI\_Win\_create**](mpi-win-create-function.md).

In the case of a window created with [**MPI\_Win\_create\_dynamic**](mpi-win-create-dynamic-function.md), the *target_disp* for all RMA functions is the address at the target; i.e., the effective *window_base* is **MPI\_BOTTOM** and the *disp_unit* is one. For dynamic windows, the *target_disp* argument to RMA communication operations is not restricted to non-negative values. Users should use [**MPI\_Get\_address**](mpi-get-address-function.md) at the target process to determine the address of a target memory location and communicate this address to the origin process.

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

