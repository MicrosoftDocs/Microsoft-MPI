---
title: MPI_Unpack_external function
TOCTitle: MPI_Unpack_external function
ms:assetid: 6b96b349-619d-4ebd-b33a-a647c5e179ea
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520586(v=VS.85)
ms:contentKeyID: 59361057
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_UNPACK_EXTERNAL
- mpif/MPI_Unpack_external
- mpi/MPI_UNPACK_EXTERNAL
dev_langs:
- C++
- C
---

# MPI\_Unpack\_external function

Unpack a buffer (packed with [**MPI\_Pack\_external**](mpi-pack-external-function.md)) according to a datatype into contiguous memory.

## Syntax

``` c++
int MPIAPI MPI_Unpack_external(
        _In_z_ char                 *datarep,
        _In_bytecount_(insize) void *inbuf,
        MPI_Aint                    insize,
        _Inout_ MPI_Aint            *position,
  _Out_ void                        *outbuf,
        int                         outcount,
        MPI_Datatype                datatype
);
```

## Parameters

  - *datarep*  
    Data representation.

  - *inbuf*  
    Start address of the input buffer.

  - *insize*  
    Input buffer size, in bytes.

  - *position*  
    Current position in buffer, in bytes.

  - *outbuf* \[out\]  
    Start address of the output buffer.

  - *outcount*  
    Number of output data items.

  - *datatype*  
    Datatype of output data item.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_UNPACK_EXTERNAL(DATAREP, INBUF, INSIZE, POSITION, OUTBUF, OUTCOUNT,
                DATATYPE, IERROR)
        INTEGER OUTCOUNT, DATATYPE, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) INSIZE, POSITION
        CHARACTER*(*) DATAREP
        <type> INBUF(*), OUTBUF(*)
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

