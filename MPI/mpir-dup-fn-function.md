---
title: MPIR_Dup_fn function
TOCTitle: MPIR_Dup_fn function
ms:assetid: d3982ec6-a490-4c6b-b1ff-01fb9b458e12
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn502493(v=VS.85)
ms:contentKeyID: 59360765
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPIR_Dup_fn
- MPIR_Dup_fn
dev_langs:
- C++
- C
description: Explore the MPIR_Dup_fn function on Microsoft's learning platform. Understand its syntax, parameters, return value, and requirements for successful implementation.
---

# MPIR\_Dup\_fn function

Simple-mindedly copies the attributes.

## Syntax

``` c++
int MPIAPI MPIR_Dup_fn(
           MPI_Comm oldcomm,
           int      keyval,
  _In_opt_ void     *extra_state,
  _In_     void     *attribute_val_in,
  _Out_    void     *attribute_val_out,
  _Out_    int      *flag
);
```

## Parameters

  - *oldcomm*  
    Communicator, ignored in current implementation.

  - *keyval*  
    Key value, ignored in current implementation.

  - *extra\_state* \[in, optional\]  
    Extra state, ignored in current implementation.

  - *attribute\_val\_in* \[in\]  
    Source value.

  - *attribute\_val\_out* \[out\]  
    Destination value.

  - *flag* \[out\]  
    Indicates if the copy was sucessfull.

## Return value

**MPI\_SUCCESS**.

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
<td>Mpi.h</td>
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

[MPI Miscellaneous Functions](mpi-miscellaneous-functions.md)

