---
title: MPI_Pcontrol function
TOCTitle: MPI_Pcontrol function
ms:assetid: 1b30a36b-bb5f-4c36-8e77-f763eb4b3ed5
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473445(v=VS.85)
ms:contentKeyID: 59360980
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_PCONTROL
- mpif/MPI_Pcontrol
- mpi/MPI_PCONTROL
dev_langs:
- C++
- C
---

# MPI\_Pcontrol function

Controls profiling.

## Syntax

``` c++
int MPIAPI MPI_Pcontrol(
   const int level,
             ...
);
```

## Parameters

  - *level*  
    Profiling level.

  - *...*  
    Other arguments (see remarks).

## Return value

**MPI\_SUCCESS**

## Fortran

``` FORTRAN
    MPI_PCONTROL(LEVEL)
        INTEGER LEVEL
```

## Remarks

This routine provides a common interface for profiling control.  The interpretation of *level* and any other arguments is left to the profiling library.  The intention is that a profiling library will provide a replacement for this routine and define the interpretation of the parameters.

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

[MPI Miscellaneous Functions](mpi-miscellaneous-functions.md)

