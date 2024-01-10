---
title: MPI_Alloc_mem function
TOCTitle: MPI_Alloc_mem function
ms:assetid: 7300a020-c7e1-4862-b604-e7e14b86aa65
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn502502(v=VS.85)
ms:contentKeyID: 59360774
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ALLOC_MEM
- mpif/MPI_Alloc_mem
- mpi/MPI_ALLOC_MEM
dev_langs:
- C++
- C
description: Learn how to allocate memory for message passing and RMA using the MPI_Alloc_mem function on Microsoft's official site.
---

# MPI\_Alloc\_mem function

Allocate memory for message passing and RMA

## Syntax

``` c++
int MPIAPI MPI_Alloc_mem(
        MPI_Aint size,
        MPI_Info info,
  _Out_ void     *baseptr
);
```

## Parameters

  - *size*  
    Size of memory segment in bytes.

  - *info*  
    Info argument.

  - *baseptr* \[out\]  
    Pointer to beginning of memory segment allocated.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_ALLOC_MEM(SIZE, INFO, BASEPTR, IERROR)
        INTEGER INFO, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) SIZE, BASEPTR
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

[MPI Management Functions](mpi-management-functions.md)

