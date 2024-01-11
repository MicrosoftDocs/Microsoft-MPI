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
description: Learn how to use the MPI_Reduce_local function in Microsoft's HPC Pack. Understand syntax, parameters, and return values for successful implementation.
---

# MPI\_Reduce\_local function

Applies a reduction operator to local arguments.

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
    Address of the input buffer.

  - *inoutbuf*  
    Address of input-output buffer.

  - *count*  
    Number of elements in each buffer.

  - *datatype*  
    Datatype of elements in the buffers.

  - *op*  
    Reduction operation.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_REDUCE_LOCAL(INBUF, INOUTBUF, COUNT, DATATYPE, OP, IERROR)
        <type> INBUF(*), INOUTBUF(*)
        INTEGER COUNT, DATATYPE, OP, IERROR
```

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

[MPI Collective Functions](mpi-collective-functions.md)

