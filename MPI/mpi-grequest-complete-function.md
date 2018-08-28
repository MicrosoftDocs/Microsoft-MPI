---
title: MPI_Grequest_complete function
TOCTitle: MPI_Grequest_complete function
ms:assetid: c4a394ed-bdce-4cf0-b26e-276716bbc707
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473391(v=VS.85)
ms:contentKeyID: 59360927
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GREQUEST_COMPLETE
- mpif/MPI_GREQUEST_COMPLETE
- mpi/MPI_GREQUEST_COMPLETE
dev_langs:
- C++
- C
---

# MPI\_Grequest\_complete function

TBD

## Syntax

``` c++
int MPIAPI MPI_Grequest_complete(
   MPI_Request request
);
```

## Parameters

  - *request*  
    TBD

## Return value

TBD

## Fortran

    MPI_GREQUEST_COMPLETE(REQUEST, IERROR)
        INTEGER REQUEST, IERROR

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

[MPI External Functions](mpi-external-functions.md)

