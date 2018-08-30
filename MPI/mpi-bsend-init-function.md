---
title: MPI_Bsend_init function
TOCTitle: MPI_Bsend_init function
ms:assetid: 42523711-0675-48d3-b91d-1a569cd287e4
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473239(v=VS.85)
ms:contentKeyID: 59360785
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_BSEND_INIT
- mpif/MPI_Bsend_init
- mpi/MPI_BSEND_INIT
dev_langs:
- C++
- C
---

# MPI\_Bsend\_init function

Builds a handle for a buffered send.

## Syntax

``` c++
int MPIAPI MPI_Bsend_init(
  _In_  void         *buf,
        int          count,
        MPI_Datatype datatype,
        int          dest,
        int          tag,
        MPI_Comm     comm,
  _Out_ MPI_Request  *request
);
```

## Parameters

  - *buf* \[in\]  
    Initial address of send buffer.

  - *count*  
    Number of elements sent.

  - *datatype*  
    Type of each element.

  - *dest*  
    Rank of destination.

  - *tag*  
    Message tag.

  - *comm*  
    Communicator.

  - *request* \[out\]  
    Communication request.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_BSEND_INIT(BUF, COUNT, DATATYPE, DEST, TAG, COMM, REQUEST, IERROR)
        <type> BUF(*)
        INTEGER COUNT, DATATYPE, DEST, TAG, COMM, REQUEST, IERROR

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

