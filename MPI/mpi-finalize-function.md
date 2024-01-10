---
title: MPI_Finalize function
TOCTitle: MPI_Finalize function
ms:assetid: e93c2023-9526-466a-892d-f11d18bb9bfe
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473372(v=VS.85)
ms:contentKeyID: 59360908
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FINALIZE
- mpif/MPI_Finalize
- mpi/MPI_FINALIZE
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Finalize
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn about the MPI_Finalize function on Microsoft's platform. Understand its syntax, parameters, return value, and how it impacts MPI processes.
---

# MPI\_Finalize function

Terminates the calling MPI process’s execution environment.

## Syntax

``` c++
int MPIAPI MPI_Finalize(void);
```

## Parameters

This function has no parameters.

## Return value

**MPI\_SUCCESS** if the function returns successfully. Other error codes if the call failed for other reasons (such as invalid arguments). In Fortran the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FINALIZE(IERROR)
        INTEGER IERROR
```

## Remarks

All MPI Processes must call this routine before exiting on the thread that called [**MPI\_Init**](mpi-init-function.md) or [**MPI\_Init\_thread**](mpi-init-thread-function.md).

The **MPI\_Finalize** function cleans up all state related to MPI. Once it is called, no other MPI functions may be called, including [**MPI\_Init**](mpi-init-function.md) and [**MPI\_Init\_thread**](mpi-init-thread-function.md). The application must ensure that all pending communications are completed or canceled before calling **MPI\_Finalize**.

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

[**MPI\_Init**](mpi-init-function.md)

[**MPI\_Init\_thread**](mpi-init-thread-function.md)

