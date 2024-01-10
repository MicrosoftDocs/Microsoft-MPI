---
title: MPI_Unpack function
TOCTitle: MPI_Unpack function
ms:assetid: 8575ee33-58a8-45dd-84c7-968f3ffe3fa5
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520585(v=VS.85)
ms:contentKeyID: 59361056
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_UNPACK
- mpif/MPI_Unpack
- mpi/MPI_UNPACK
dev_langs:
- C++
- C
description: Learn how to unpack a buffer into contiguous memory using the MPI_Unpack function on Microsoft's official site.
---

# MPI\_Unpack function

Unpacks a buffer according to a datatype into contiguous memory.

## Syntax

``` c++
int MPIAPI MPI_Unpack(
        _In_bytecount_(insize) void *inbuf,
        int                         insize,
        _Inout_ int                 *position,
  _Out_ void                        *outbuf,
        int                         outcount,
        MPI_Datatype                datatype,
        MPI_Comm                    comm
);
```

## Parameters

  - *inbuf*  
    Start address of the input buffer.

  - *insize*  
    Size of input buffer, in bytes.

  - *position*  
    Current position in bytes.

  - *outbuf* \[out\]  
    Start address of the output buffer.

  - *outcount*  
    Number of items to be unpacked.

  - *datatype*  
    Datatype of each output data item.

  - *comm*  
    Communicator for packed message.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_UNPACK(INBUF, INSIZE, POSITION, OUTBUF, OUTCOUNT, DATATYPE, COMM, IERROR)
        <type> INBUF(*), OUTBUF(*)
        INTEGER INSIZE, POSITION, OUTCOUNT, DATATYPE, COMM, IERROR
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

[MPI Datatype Functions](mpi-datatype-functions.md)

