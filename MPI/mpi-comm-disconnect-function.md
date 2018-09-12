---
title: MPI_Comm_disconnect function
TOCTitle: MPI_Comm_disconnect function
ms:assetid: 29696257-76c8-4e5f-8a0f-f748d4844476
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473266(v=VS.85)
ms:contentKeyID: 59360812
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_DISCONNECT
- mpif/MPI_Comm_disconnect
- mpi/MPI_COMM_DISCONNECT
dev_langs:
- C++
- C
---

# MPI\_Comm\_disconnect function

Disconnect from a communicator.

## Syntax

``` c++
int MPIAPI MPI_Comm_disconnect(
  _In_ MPI_Comm *comm
);
```

## Parameters

  - *comm* \[in\]  
    Communicator.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMM_DISCONNECT(COMM, IERROR)
        INTEGER COMM, IERROR
```

## Remarks

This routine waits for all pending communication to complete, then frees the communicator and sets *comm* to **MPI\_COMM\_NULL**.  It may not be called with **MPI\_COMM\_WORLD** or **MPI\_COMM\_SELF**.

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

[MPI Process Management Functions](mpi-process-management-functions.md)

