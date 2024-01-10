---
title: MPI_Error_class function
TOCTitle: MPI_Error_class function
ms:assetid: 7bdf56d4-dd68-4245-a585-187e3c62723c
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473299(v=VS.85)
ms:contentKeyID: 59360845
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ERROR_CLASS
- mpif/MPI_Error_class
- mpi/MPI_ERROR_CLASS
dev_langs:
- C++
- C
---

# MPI\_Error\_class function

Converts an error code into an error class.

## Syntax

``` c++
int MPIAPI MPI_Error_class(
        int errorcode,
  _Out_ int *errorclass
);
```

## Parameters

  - *errorcode*  
    Error code returned by an MPI routine.

  - *errorclass* \[out\]  
    Error class associated with *errorcode*.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_ERROR_CLASS(ERRORCODE, ERRORCLASS, IERROR)
        INTEGER ERRORCODE, ERRORCLASS, IERROR
```

## Requirements

<table>
<colgroup>
<col  />
<col  />
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

