---
title: MPI_File_create_errhandler function
TOCTitle: MPI_File_create_errhandler function
ms:assetid: fc15dd34-c897-43a1-8e5c-8b37a90d1664
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473306(v=VS.85)
ms:contentKeyID: 59360852
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_CREATE_ERRHANDLER
- mpif/MPI_File_create_errhandler
- mpi/MPI_FILE_CREATE_ERRHANDLER
dev_langs:
- C++
- C
---

# MPI\_File\_create\_errhandler function

TBD

## Syntax

``` c++
int MPIAPI MPI_File_create_errhandler(
  _In_  MPI_File_errhandler_fn *function,
  _Out_ MPI_Errhandler         *errhandler
);
```

## Parameters

  - *function* \[in\]  
    TBD

  - *errhandler* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_FILE_CREATE_ERRHANDLER(FILE_ERRHANDLER_FN, ERRHANDLER, IERROR)
        EXTERNAL FILE_ERRHANDLER_FN
        INTEGER ERRHANDLER, IERROR

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

[*MPI\_File\_errhandler\_fn*](mpi-file-errhandler-fn-callback-function.md)

