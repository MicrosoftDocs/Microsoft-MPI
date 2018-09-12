---
title: MPI_Comm_free_keyval function
TOCTitle: MPI_Comm_free_keyval function
ms:assetid: 9f5c82d0-29b4-4c5f-9a84-1a9e3e26690a
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473270(v=VS.85)
ms:contentKeyID: 59360816
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_FREE_KEYVAL
- mpif/MPI_Comm_free_keyval
- mpi/MPI_COMM_FREE_KEYVAL
dev_langs:
- C++
- C
---

# MPI\_Comm\_free\_keyval function

Frees an extant attribute key.

## Syntax

``` c++
int MPIAPI MPI_Comm_free_keyval(
   _Inout_ int *comm_keyval
);
```

## Parameters

  - *comm\_keyval*  
    Key value.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMM_FREE_KEYVAL(COMM_KEYVAL, IERROR)
        INTEGER COMM_KEYVAL, IERROR
```

## Remarks

This function sets the value of keyval to **MPI\_KEYVAL\_INVALID**. Note that it is not erroneous to free an attribute key that is in use, because the actual free does not transpire until after all references (in other communicators on the process) to the key have been freed. These references need to be explictly freed by the program, either via calls to [**MPI\_Comm\_delete\_attr**](mpi-comm-delete-attr-function.md) that free one attribute instance, or by calls to [**MPI\_Comm\_free**](mpi-comm-free-function.md) that free all attribute instances associated with the freed communicator.

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

[MPI Caching Functions](mpi-caching-functions.md)

