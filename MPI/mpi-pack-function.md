---
title: MPI_Pack function
TOCTitle: MPI_Pack function
ms:assetid: f518e8c8-43b7-447d-a5c4-4e8de9a51eb2
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473440(v=VS.85)
ms:contentKeyID: 59360976
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_PACK
- mpif/MPI_Pack
- mpi/MPI_PACK
dev_langs:
- C++
- C
description: Learn about the MPI_Pack function on Microsoft's official site. Understand its syntax, parameters, return values, and requirements for successful implementation.
---

# MPI\_Pack function

Packs a datatype into contiguous memory.

## Syntax

``` c++
int MPIAPI MPI_Pack(
  _In_ void                        *inbuf,
       int                         incount,
       MPI_Datatype                datatype,
       _Out_bytecap_(outsize) void *outbuf,
       int                         outsize,
       _Inout_ int                 *position,
       MPI_Comm                    comm
);
```

## Parameters

  - *inbuf* \[in\]  
    Start address of the input buffer.

  - *incount*  
    Number of input data items.

  - *datatype*  
    Datatype of each input data item.

  - *outbuf*
    Start address of the output buffer.

  - *outsize*  
    Output buffer size, in bytes.

  - *position*  
    Current position in buffer, in bytes.

  - *comm*  
    Communicator for packed message.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_PACK(INBUF, INCOUNT, DATATYPE, OUTBUF, OUTSIZE, POSITION, COMM, IERROR)
        <type> INBUF(*), OUTBUF(*)
        INTEGER INCOUNT, DATATYPE, OUTSIZE, POSITION, COMM, IERROR
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

[MPI Datatype Functions](mpi-datatype-functions.md)

