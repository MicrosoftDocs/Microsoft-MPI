---
title: MPI_Exscan function
TOCTitle: MPI_Exscan function
ms:assetid: 21ee8f78-d70e-4886-927d-f810f2f933e6
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473301(v=VS.85)
ms:contentKeyID: 59360847
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_EXSCAN
- mpif/MPI_Exscan
- mpi/MPI_EXSCAN
dev_langs:
- C++
- C
---

# MPI\_Exscan function

Computes the exclusive scan (partial reductions) of data on a collection of processes.

## Syntax

``` c++
int MPIAPI MPI_Exscan(
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
    Data type of elements of input buffer.

  - *op*  
    Operation.

  - *comm*  
    Communicator.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_EXSCAN(SENDBUF, RECVBUF, COUNT, DATATYPE, OP, COMM, IERROR)
        <type> SENDBUF(*), RECVBUF(*)
        INTEGER COUNT, DATATYPE, OP, COMM, IERROR

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

[MPI Collective Functions](mpi-collective-functions.md)

