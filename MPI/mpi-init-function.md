---
title: MPI_Init function
TOCTitle: MPI_Init function
ms:assetid: 4b88878f-b15c-421e-bad0-21353b516bb5
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473419(v=VS.85)
ms:contentKeyID: 59360955
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_INIT
- mpif/MPI_Init
- mpi/MPI_INIT
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Init
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Master the MPI_Init function for single-threaded execution with our comprehensive guide. Learn syntax, parameters, return values, and more.
---

# MPI\_Init function

Initializes the calling MPI process’s execution environment for single threaded execution.

## Syntax

``` c++
int MPIAPI MPI_Init(
  _In_opt_ int                        *argc,
           _In_opt_count_(*argc) char ***argv
);
```

## Parameters

  - *argc* \[in, optional\]  
    A pointer to the number of arguments for the program. This value can be NULL.

  - *argv*  
    A pointer to the argument list for the program. This value can be NULL.

## Return value

**MPI\_SUCCESS** if the function returns successfully. Other error codes if the call failed for other reasons (such as invalid arguments). In Fortran the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_INIT(IERROR)
        INTEGER IERROR
```

## Remarks

This function must be called by one thread only. That thread will be known as the “Main Thread” and must be the same thread to call [**MPI\_Finalize**](mpi-finalize-function.md).

The Fortran binding of **MPI\_Init** does not accept the ARGC and ARGV parameters.

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

[**MPI\_Finalize**](mpi-finalize-function.md)

[**MPI\_Init\_thread**](mpi-init-thread-function.md)

