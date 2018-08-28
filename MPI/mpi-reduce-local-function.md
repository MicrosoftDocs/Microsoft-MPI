---
title: MPI_Reduce_local function
TOCTitle: MPI_Reduce_local function
ms:assetid: 0310d14e-ebc8-4131-8467-ee58f04d0020
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473456(v=VS.85)
ms:contentKeyID: 59360991
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_REDUCE_LOCAL
- mpif/MPI_Reduce_local
- mpi/MPI_REDUCE_LOCAL
dev_langs:
- C++
- C
---

# MPI\_Reduce\_local function

TBD

## Syntax

``` c++
int MPIAPI MPI_Reduce_local(
  _In_ void         *inbuf,
       _Inout_ void *inoutbuf,
       int          count,
       MPI_Datatype datatype,
       MPI_Op       op
);
```

## Parameters

  - *inbuf* \[in\]  
    TBD

  - *inoutbuf*  
    TBD

  - *count*  
    TBD

  - *datatype*  
    TBD

  - *op*  
    TBD

## Return value

TBD

## Fortran

    MPI_REDUCE_LOCAL(INBUF, INOUTBUF, COUNT, DATATYPE, OP, IERROR)
        <type> INBUF(*), INOUTBUF(*)
        INTEGER COUNT, DATATYPE, OP, IERROR

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

[MPI Collective Functions](mpi-collective-functions.md)

