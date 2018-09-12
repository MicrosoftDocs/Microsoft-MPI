---
title: MPI_Pack_size function
TOCTitle: MPI_Pack_size function
ms:assetid: da4f6f13-89d5-47bb-9fc5-0d7b3fd1bd5b
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473443(v=VS.85)
ms:contentKeyID: 59360979
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_PACK_SIZE
- mpif/MPI_Pack_size
- mpi/MPI_PACK_SIZE
dev_langs:
- C++
- C
---

# MPI\_Pack\_size function

Returns the upper bound on the amount of space needed to pack a message.

## Syntax

``` c++
int MPIAPI MPI_Pack_size(
        int          incount,
        MPI_Datatype datatype,
        MPI_Comm     comm,
  _Out_ int          *size
);
```

## Parameters

  - *incount*  
    Count argument to packing call.

  - *datatype*  
    Datatype argument to packing call.

  - *comm*  
    Communicator argument to packing call.

  - *size* \[out\]  
    Upper bound on size of packed message, in bytes.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_PACK_SIZE(INCOUNT, DATATYPE, COMM, SIZE, IERROR)
        INTEGER INCOUNT, DATATYPE, COMM, SIZE, IERROR
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

[MPI Datatype Functions](mpi-datatype-functions.md)

