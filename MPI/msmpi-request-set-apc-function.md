---
title: MSMPI_Request_set_apc function
TOCTitle: MSMPI_Request_set_apc function
ms:assetid: dff831d6-4505-49fe-856e-05b9241682db
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520626(v=VS.85)
ms:contentKeyID: 59361097
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MSMPI_Request_set_apc
- MSMPI_Request_set_apc
dev_langs:
- C++
- C
---

# MSMPI\_Request\_set\_apc function

TBD

## Syntax

``` c++
int MPIAPI MSMPI_Request_set_apc(
       MPI_Request            request,
  _In_ MSMPI_Request_callback *callback_fn,
  _In_ MPI_Status             *callback_status
);
```

## Parameters

  - *request*  
    TBD

  - *callback\_fn* \[in\]  
    TBD

  - *callback\_status* \[in\]  
    TBD

## Return value

TBD

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

[**MSMPI\_Request\_callback**](msmpi-request-callback-function.md)

