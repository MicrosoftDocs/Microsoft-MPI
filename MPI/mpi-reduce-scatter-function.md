---
title: MPI_Reduce_scatter function
TOCTitle: MPI_Reduce_scatter function
ms:assetid: f52cf815-485f-4cca-903f-a0179ff929ed
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473457(v=VS.85)
ms:contentKeyID: 59360992
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_REDUCE_SCATTER
- mpif/MPI_Reduce_scatter
- mpi/MPI_REDUCE_SCATTER
dev_langs:
- C++
- C
description: Master the MPI_Reduce_scatter function with this comprehensive guide. Learn syntax, parameters, and return values for successful implementation.
---

# MPI\_Reduce\_scatter function

Combines values and scatters the results.

## Syntax

``` c++
int MPIAPI MPI_Reduce_scatter(
  _In_  void         *sendbuf,
  _Out_ void         *recvbuf,
  _In_  int          *recvcounts,
        MPI_Datatype datatype,
        MPI_Op       op,
        MPI_Comm     comm
);
```

## Parameters

  - *sendbuf* \[in\]  
    Starting address of send buffer.

  - *recvbuf* \[out\]  
    Starting address of receive buffer.

  - *recvcounts* \[in\]  
    Integer array specifying the number of elements in result distributed to each process.

  - *datatype*  
    Datatype of elements of input buffer.

  - *op*  
    Operation.

  - *comm*  
    Communicator.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_REDUCE_SCATTER(SENDBUF, RECVBUF, RECVCOUNTS, DATATYPE, OP, COMM, IERROR)
        <type> SENDBUF(*), RECVBUF(*)
        INTEGER RECVCOUNTS(*), DATATYPE, OP, COMM, IERROR
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

[MPI Collective Functions](mpi-collective-functions.md)

