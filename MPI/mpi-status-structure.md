﻿---
title: MPI_Status structure
TOCTitle: MPI_Status structure
ms:assetid: E7F73B45-7A00-4210-AAAC-0A3A4EE186B6
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473475(v=VS.85)
ms:contentKeyID: 59361010
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_Status
- mpi/PMPI_Status
- MPI_Status
- PMPI_Status
dev_langs:
- C++
- C
---

# MPI\_Status structure

Structure that represents the status of the received message.

## Syntax

``` c++
typedef struct _MPI_Status {
  int count;
  int cancelled;
  int MPI_SOURCE;
  int MPI_TAG;
  int MPI_ERROR;
} MPI_Status, *PMPI_Status;
```

## Members

  - **count**  
    Number of received entries.

  - **cancelled**
    
    Indication if the corresponding request was cancelled.

  - **MPI\_SOURCE**
    
    Source of the message.

  - **MPI\_TAG**
    
    Tag value of the message.

  - **MPI\_ERROR**
    
    Error, associated with the message.

## Remarks

There are two defined **MPI\_Status** pointers that can be used in place of this structure, **MPI\_STATUS\_IGNORE** and **MPI\_STATUSES\_IGNORE**.

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
</tbody>
</table>


## See also

[MPI Structs](mpi-structs.md)

