﻿---
title: MPI_Get_elements function
TOCTitle: MPI_Get_elements function
ms:assetid: e9d2d957-a9ea-4efe-ac2a-b69844ee6712
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473381(v=VS.85)
ms:contentKeyID: 59360917
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GET_ELEMENTS
- mpif/MPI_Get_elements
- mpi/MPI_GET_ELEMENTS
dev_langs:
- C++
- C
---

# MPI\_Get\_elements function

Returns the number of basic elements in a datatype.

## Syntax

``` c++
int MPIAPI MPI_Get_elements(
  _In_  MPI_Status   *status,
        MPI_Datatype datatype,
  _Out_ int          *count
);
```

## Parameters

  - *status* \[in\]  
    Return status of receive operation.

  - *datatype*  
    Datatype used by receive operation.

  - *count* \[out\]  
    Number of received basic elements.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_GET_ELEMENTS(STATUS, DATATYPE, COUNT, IERROR)
        INTEGER STATUS(MPI_STATUS_SIZE), DATATYPE, COUNT, IERROR

## Remarks

If the size of the datatype is zero and the amount of data returned as determined by *status* is also zero, this routine will return a count of zero.

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

