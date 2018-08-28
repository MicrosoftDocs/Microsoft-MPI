---
title: MPI_Is_thread_main function
TOCTitle: MPI_Is_thread_main function
ms:assetid: 5ef3ecf3-d8e1-4e76-9d0b-1e0b572c1b6a
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473429(v=VS.85)
ms:contentKeyID: 59360965
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_IS_THREAD_MAIN
- mpif/MPI_Is_thread_main
- mpi/MPI_IS_THREAD_MAIN
dev_langs:
- C++
- C
---

# MPI\_Is\_thread\_main function

TBD

## Syntax

``` c++
int MPIAPI MPI_Is_thread_main(
  _Out_ int *flag
);
```

## Parameters

  - *flag* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_IS_THREAD_MAIN(FLAG, IERROR)
        LOGICAL FLAG
        INTEGER IERROR

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

[MPI External Functions](mpi-external-functions.md)

