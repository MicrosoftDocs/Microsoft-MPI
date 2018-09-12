---
title: MPI_Recv_init function
TOCTitle: MPI_Recv_init function
ms:assetid: a47e0891-c684-43cd-b831-5c2fc45ed6aa
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473454(v=VS.85)
ms:contentKeyID: 59360989
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_RECV_INIT
- mpif/MPI_Recv_init
- mpi/MPI_RECV_INIT
dev_langs:
- C++
- C
---

# MPI\_Recv\_init function

Creates a persistent request for a receive.

## Syntax

``` c++
int MPIAPI MPI_Recv_init(
  _Out_ void         *buf,
        int          count,
        MPI_Datatype datatype,
        int          source,
        int          tag,
        MPI_Comm     comm,
  _Out_ MPI_Request  *request
);
```

## Parameters

  - *buf* \[out\]  
    Initial address of receive buffer.

  - *count*  
    Number of elements received.

  - *datatype*  
    Type of each element.

  - *source*  
    Rank of source, or **MPI\_ANY\_SOURCE**.

  - *tag*  
    Message tag, or **MPI\_ANY\_TAG**.

  - *comm*  
    Communicator.

  - *request* \[out\]  
    Communication request.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_RECV_INIT(BUF, COUNT, DATATYPE, SOURCE, TAG, COMM, REQUEST, IERROR)
        <type> BUF(*)
        INTEGER COUNT, DATATYPE, SOURCE, TAG, COMM, REQUEST, IERROR
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

