---
title: MPI_Probe function
TOCTitle: MPI_Probe function
ms:assetid: 48c0aa71-76be-402f-8318-6fed9a8d2667
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473447(v=VS.85)
ms:contentKeyID: 59360982
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_PROBE
- mpif/MPI_Probe
- mpi/MPI_PROBE
dev_langs:
- C++
- C
---

# MPI\_Probe function

Blocking test for a message.

## Syntax

``` c++
int MPIAPI MPI_Probe(
        int        source,
        int        tag,
        MPI_Comm   comm,
  _Out_ MPI_Status *status
);
```

## Parameters

  - *source*  
    Source rank, or **MPI\_ANY\_SOURCE**.

  - *tag*  
    Tag value, or **MPI\_ANY\_TAG**.

  - *comm*  
    Communicator.

  - *status* \[out\]  
    Status object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_PROBE(SOURCE, TAG, COMM, STATUS, IERROR)
        INTEGER SOURCE, TAG, COMM, STATUS(MPI_STATUS_SIZE), IERROR

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

