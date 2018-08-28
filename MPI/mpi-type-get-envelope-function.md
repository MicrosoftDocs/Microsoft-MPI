---
title: MPI_Type_get_envelope function
TOCTitle: MPI_Type_get_envelope function
ms:assetid: 5a7b663b-d716-4a42-a4e3-4f3993e7bcb8
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520570(v=VS.85)
ms:contentKeyID: 59361041
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_GET_ENVELOPE
- mpif/MPI_Type_get_envelope
- mpi/MPI_TYPE_GET_ENVELOPE
dev_langs:
- C++
- C
---

# MPI\_Type\_get\_envelope function

TBD

## Syntax

``` c++
int MPIAPI MPI_Type_get_envelope(
        MPI_Datatype datatype,
  _Out_ int          *num_integers,
  _Out_ int          *num_addresses,
  _Out_ int          *num_datatypes,
  _Out_ int          *combiner
);
```

## Parameters

  - *datatype*  
    TBD

  - *num\_integers* \[out\]  
    TBD

  - *num\_addresses* \[out\]  
    TBD

  - *num\_datatypes* \[out\]  
    TBD

  - *combiner* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_TYPE_GET_ENVELOPE(DATATYPE, NUM_INTEGERS, NUM_ADDRESSES, NUM_DATATYPES,
                COMBINER, IERROR)
        INTEGER DATATYPE, NUM_INTEGERS, NUM_ADDRESSES, NUM_DATATYPES, COMBINER,
        IERROR

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

