---
title: MSMPI_Get_bsend_overhead function
TOCTitle: MSMPI_Get_bsend_overhead function
ms:assetid: a12d3296-e784-46b7-bc94-5ac5912566dc
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520620(v=VS.85)
ms:contentKeyID: 59361091
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MSMPI_Get_bsend_overhead
- MSMPI_Get_bsend_overhead
dev_langs:
- C++
- C
---

# MSMPI\_Get\_bsend\_overhead function

Returns the size of the overhead required for Bsend buffers.

## Syntax

``` c++
int MPIAPI MSMPI_Get_bsend_overhead(void);
```

## Parameters

This function has no parameters.

## Return value

The required overhead for Bsend operations.

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

[MPI Miscellaneous Functions](mpi-miscellaneous-functions.md)

