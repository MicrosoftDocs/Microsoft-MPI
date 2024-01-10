---
title: MSMPI_Request_callback function
TOCTitle: MSMPI_Request_callback function
ms:assetid: d07a68ea-edd0-4471-99c0-0e69e1a5c8a5
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520625(v=VS.85)
ms:contentKeyID: 59361096
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MSMPI_Request_callback
- MSMPI_Request_callback
dev_langs:
- C++
- C
---

# MSMPI\_Request\_callback function

This is a placeholder for application-defined APC callback function.

## Syntax

``` c++
void MSMPI_Request_callback(
  _In_ MPI_Status *status
);
```

## Parameters

  - *status* \[in\]  
    MPI status object.

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

