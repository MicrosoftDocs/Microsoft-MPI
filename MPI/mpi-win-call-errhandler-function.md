---
title: MPI_Win_call_errhandler function
TOCTitle: MPI_Win_call_errhandler function
ms:assetid: f801a8d2-f467-43ce-b4e4-e6096d3013ff
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520593(v=VS.85)
ms:contentKeyID: 59361064
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WIN_CALL_ERRHANDLER
- mpif/MPI_Win_call_errhandler
- mpi/MPI_WIN_CALL_ERRHANDLER
dev_langs:
- C++
- C
---

# MPI\_Win\_call\_errhandler function

Call the error handler installed on a window object.

## Syntax

``` c++
int MPIAPI MPI_Win_call_errhandler(
   MPI_Win win,
   int     errcode
);
```

## Parameters

  - *win*  
    Window with error handler.

  - *errcode*  
    Error code.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WIN_CALL_ERRHANDLER(WIN, ERRORCODE, IERROR)
        INTEGER WIN, ERRORCODE, IERROR
```

## Remarks

Assuming the input parameters are valid, when the error handler is set to **MPI\_ERRORS\_RETURN**, this routine will always return **MPI\_SUCCESS**.

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

[MPI Management Functions](mpi-management-functions.md)

