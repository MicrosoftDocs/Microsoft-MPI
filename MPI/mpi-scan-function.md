---
title: MPI_Scan function
TOCTitle: MPI_Scan function
ms:assetid: d7d4782a-6140-4696-99a8-849efb219ea8
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473464(v=VS.85)
ms:contentKeyID: 59360999
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_SCAN
- mpif/MPI_Scan
- mpi/MPI_SCAN
dev_langs:
- C++
- C
description: Learn about the MPI_Scan function on Microsoft's official site. Understand its syntax, parameters, return values, and related requirements.
---

# MPI\_Scan function

Computes the scan (partial reductions) of data on a collection of processes.

## Syntax

``` c++
int MPIAPI MPI_Scan(
  _In_  void         *sendbuf,
  _Out_ void         *recvbuf,
        int          count,
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

  - *count*  
    Number of elements in input buffer.

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
    MPI_SCAN(SENDBUF, RECVBUF, COUNT, DATATYPE, OP, COMM, IERROR)
        <type> SENDBUF(*), RECVBUF(*)
        INTEGER COUNT, DATATYPE, OP, COMM, IERROR
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

[MPI Collective Functions](mpi-collective-functions.md)

