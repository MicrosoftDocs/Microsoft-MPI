---
title: MPI_Win_test function
TOCTitle: MPI_Win_test function
ms:assetid: d43eee70-534a-4f0f-a5cd-fb442a809fe2
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520615(v=VS.85)
ms:contentKeyID: 59361086
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_TEST
- mpif/MPI_Win_test
- mpi/MPI_WIN_TEST
dev_langs:
- C++
- C
---

# MPI\_Win\_test function

Test whether an RMA exposure epoch has completed.

## Syntax

``` c++
int MPIAPI MPI_Win_test(
        MPI_Win win,
  _Out_ int     *flag
);
```

## Parameters

  - *win*  
    Window object.

  - *flag* \[out\]  
    Success flag.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_TEST(WIN, FLAG, IERROR)
        INTEGER WIN, IERROR
        LOGICAL FLAG
```

## Remarks

This is the nonblocking version of [**MPI\_Win\_wait**](mpi-win-wait-function.md).

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

