---
title: MPI_Comm_test_inter function
TOCTitle: MPI_Comm_test_inter function
ms:assetid: a70de0d0-e4f1-4215-a31d-d482a0606f8c
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473287(v=VS.85)
ms:contentKeyID: 59360833
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_TEST_INTER
- mpif/MPI_Comm_test_inter
- mpi/MPI_COMM_TEST_INTER
dev_langs:
- C++
- C
---

# MPI\_Comm\_test\_inter function

TBD

## Syntax

``` c++
int MPIAPI MPI_Comm_test_inter(
        MPI_Comm comm,
  _Out_ int      *flag
);
```

## Parameters

  - *comm*  
    TBD

  - *flag* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_COMM_TEST_INTER(COMM, FLAG, IERROR)
        INTEGER COMM, IERROR
        LOGICAL FLAG

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

[MPI Communicator Functions](mpi-communicator-functions.md)

