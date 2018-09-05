---
title: MPI_Op_free function
TOCTitle: MPI_Op_free function
ms:assetid: e18b71d1-4e7a-46b8-b08c-ee256296488a
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473439(v=VS.85)
ms:contentKeyID: 59360975
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_Op_free
- mpi/MPI_SCATTER
- MPI_Op_free
- MPI_SCATTER
- mpif/MPI_Op_free
- mpif/MPI_SCATTER
dev_langs:
- C++
- C
---

# MPI\_Op\_free function

Frees a user-defined combination function handle.

## Syntax

``` c++
int MPIAPI MPI_Op_free(
   _Inout_ MPI_Op *op
);
```

## Parameters

  - *op*  
    Operation.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_OP_FREE(OP, IERROR)
        INTEGER OP, IERROR

## Remarks

*op* is set to **MPI\_OP\_NULL** on exit.

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

