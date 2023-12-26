---
title: MPI_Iprobe function
TOCTitle: MPI_Iprobe function
ms:assetid: e2a6fadf-447d-42b1-a455-89a504beeabd
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473424(v=VS.85)
ms:contentKeyID: 59360960
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_IPROBE
- mpif/MPI_Iprobe
- mpi/MPI_IPROBE
dev_langs:
- C++
- C
description: Learn about the MPI_Iprobe function on Microsoft's official site. Understand its syntax, parameters, return values, and related requirements.
---

# MPI\_Iprobe function

Nonblocking test for a message.

## Syntax

``` c++
int MPIAPI MPI_Iprobe(
        int        source,
        int        tag,
        MPI_Comm   comm,
  _Out_ int        *flag,
  _Out_ MPI_Status *status
);
```

## Parameters

  - *source*  
    Source rank, or  **MPI\_ANY\_SOURCE**.

  - *tag*  
    Tag value, or **MPI\_ANY\_TAG**.

  - *comm*  
    Communicator.

  - *flag* \[out\]  
    True if a message with the specified source, tag, and communicator is available.

  - *status* \[out\]  
    Status object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_IPROBE(SOURCE, TAG, COMM, FLAG, STATUS, IERROR)
        LOGICAL FLAG
        INTEGER SOURCE, TAG, COMM, STATUS(MPI_STATUS_SIZE), IERROR
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

[MPI Point to Point Functions](mpi-point-to-point-functions.md)

