---
title: MPI_Status_f2c function
TOCTitle: MPI_Status_f2c function
ms:assetid: 427308ed-2fb0-411e-bab5-d3e78ad35dcd
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473477(v=VS.85)
ms:contentKeyID: 59361012
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_Status_f2c
- MPI_Status_f2c
- mpif/MPI_Status_f2c
dev_langs:
- C++
- C
description: Learn how to convert Fortran status to C status using MPI_Status_f2c function. No information is lost in the conversion. Perfect for HPC Pack users.
---

# MPI\_Status\_f2c function

Converts from a Fortran status (which is an array of integers) to a C status (which is a structure). The conversion occurs on all the information in status, including that which is hidden. That is, no status information is lost in the conversion.

## Syntax

``` c++
int MPIAPI MPI_Status_f2c(
  _In_  MPI_Fint   *f_status,
  _Out_ MPI_Status *status
);
```

## Parameters

  - *f\_status* \[in\]  
    Fortran status.

  - *status* \[out\]  
    C status.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

## Remarks

If *f\_status* is a valid Fortran status, but not the Fortran value of **MPI\_STATUS\_IGNORE** or **MPI\_STATUSES\_IGNORE**, then [**MPI\_Status\_f2c**](mpi-status-f2c-function.md) returns in *c\_status* a valid C status with the same content. If *f\_status* is the Fortran value of **MPI\_STATUS\_IGNORE** or **MPI\_STATUSES\_IGNORE**, or if *f\_status* is not a valid Fortran status, then the call is erroneous.

The C status has the same source, tag and error code values as the Fortran status, and returns the same answers when queried for count, elements, and cancellation. The conversion function may be called with a Fortran status argument that has an undefined error field, in which case the value of the error field in the C status argument is undefined

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

[MPI Miscellaneous Functions](mpi-miscellaneous-functions.md)

