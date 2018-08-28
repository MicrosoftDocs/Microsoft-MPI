---
title: MPI_Waitsome function
TOCTitle: MPI_Waitsome function
ms:assetid: aa5b1b9f-7e49-4074-adb2-3e06b889baea
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520592(v=VS.85)
ms:contentKeyID: 59361063
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WAITSOME
- mpif/MPI_Waitsome
- mpi/MPI_WAITSOME
dev_langs:
- C++
- C
---

# MPI\_Waitsome function

TBD

## Syntax

``` c++
int MPIAPI MPI_Waitsome(
        int                                         incount,
        _Inout_count_(incount) MPI_Request          array_of_requests,
  _Out_ int                                         *outcount,
        _Out_cap_post_count_(incount,*outcount) int *array_of_indices,
        _Out_cap_post_count_(incount,*outcount)     *array_of_statuses
);
```

## Parameters

  - *incount*  
    TBD

  - *array\_of\_requests*  
    TBD

  - *outcount* \[out\]  
    TBD

  - *array\_of\_indices*  
    TBD

  - *array\_of\_statuses*  
    TBD

## Return value

TBD

## Fortran

    MPI_WAITSOME(INCOUNT, ARRAY_OF_REQUESTS, OUTCOUNT, ARRAY_OF_INDICES, ARRAY_OF_STATUSES, IERROR)
        INTEGER INCOUNT, ARRAY_OF_REQUESTS(*), OUTCOUNT, ARRAY_OF_INDICES(*),
        ARRAY_OF_STATUSES(MPI_STATUS_SIZE,*), IERROR

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

[MPI Point to Point Functions](mpi-point-to-point-functions.md)

