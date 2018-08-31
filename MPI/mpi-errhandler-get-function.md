---
title: MPI_Errhandler_get function
TOCTitle: MPI_Errhandler_get function
ms:assetid: 38ae1d30-369e-4f94-bb53-050233e6dfea
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473296(v=VS.85)
ms:contentKeyID: 59360842
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ERRHANDLER_GET
- mpif/MPI_Errhandler_get
- mpi/MPI_ERRHANDLER_GET
dev_langs:
- C++
- C
---

# MPI\_Errhandler\_get function

This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Comm\_get\_errhandler**](mpi-comm-get-errhandler-function.md) function.

## Syntax

``` c++
int
MPIAPI MPI_Errhandler_get(
        MPI_Comm       comm,
  _Out_ MPI_Errhandler *errhandler
);
```

## Parameters

  - *comm*  
    Communicator to get the error handler from.

  - *errhandler* \[out\]  
    MPI error handler currently associated with communicator.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

## Fortran

``` 
```

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

[MPI Management Functions](mpi-management-functions.md)

[**MPI\_Comm\_get\_errhandler**](mpi-comm-get-errhandler-function.md)

