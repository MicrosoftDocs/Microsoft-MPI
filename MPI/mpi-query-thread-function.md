---
title: MPI_Query_thread function
TOCTitle: MPI_Query_thread function
ms:assetid: b413d76a-ce8b-4340-9334-adbbe70c905b
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473452(v=VS.85)
ms:contentKeyID: 59360987
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_QUERY_THREAD
- mpif/MPI_Query_thread
- mpi/MPI_QUERY_THREAD
dev_langs:
- C++
- C
---

# MPI\_Query\_thread function

TBD

## Syntax

``` c++
int MPIAPI MPI_Query_thread(
  _Out_ int *provided
);
```

## Parameters

  - *provided* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_QUERY_THREAD(PROVIDED, IERROR)
        INTEGER PROVIDED, IERROR

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

