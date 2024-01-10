---
title: MPI_Win_errhandler_fn callback function
TOCTitle: MPI_Win_errhandler_fn callback function
ms:assetid: cad5be1d-5e89-41d1-9548-f6eb09c14e34
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520601(v=VS.85)
ms:contentKeyID: 59361072
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_Win_errhandler_fn
- mpi/WIN_ERRHANDLER_FUNCTION
- MPI_Win_errhandler_fn
- mpif/MPI_Win_errhandler_fn
- mpif/WIN_ERRHANDLER_FUNCTION
- WIN_ERRHANDLER_FUNCTION
dev_langs:
- C++
- C
---

# MPI\_Win\_errhandler\_function callback function

*MPI\_Win\_errhandler\_function* is a placeholder for the application-defined function name.

## Syntax

``` c++
void MPI_Win_errhandler_function(
  _In_    MPI_Win *win,
  _Inout_  int    *errcode,
                  ...
);
```

## Parameters

  - *win* \[in\]  
    MPI window object in use.

  - *errcode* \[in, out\]  
    Error code to be returned.

## Fortran

``` FORTRAN
    SUBROUTINE WIN_ERRHANDLER_FUNCTION(WIN, ERROR_CODE)
        INTEGER WIN, ERROR_CODE
```

## Remarks

The placeholder name of this function, *MPI\_Win\_errhandler\_fn*, is deprecated in the MPI-2.2 standard and replaced by *MPI\_Win\_errhandler\_function*. The function prototype is unchanged.

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
</tbody>
</table>


## See also

[MPI Management Functions](mpi-management-functions.md)

[**MPI\_Win\_create\_errhandler**](mpi-win-create-errhandler-function.md)

