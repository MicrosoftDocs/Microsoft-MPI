---
title: MPI_Comm enumeration
TOCTitle: MPI_Comm enumeration
ms:assetid: 41201F26-5B85-49AB-A138-46CC9864B180
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473254(v=VS.85)
ms:contentKeyID: 59360800
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_Comm
- mpi/MPI_COMM_NULL
- mpi/MPI_COMM_SELF
- mpi/MPI_COMM_WORLD
- MPI_Comm
- MPI_COMM_NULL
- MPI_COMM_SELF
- MPI_COMM_WORLD
dev_langs:
- C++
- C
---

# MPI\_Comm enumeration

## Syntax

``` c++
typedef enum _MPI_Comm { 
  MPI_COMM_NULL   = 0x04000000,
  MPI_COMM_WORLD  = 0x44000000,
  MPI_COMM_SELF   = 0x44000001
} MPI_Comm;
```

## Constants

  - **MPI\_COMM\_NULL**  
    The value used for invalid communicator handles.

  - **MPI\_COMM\_WORLD**  
    An initial intra-communicator of all processes.

  - **MPI\_COMM\_SELF**  
    Communicator that contains only the calling process.

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

[MPI Enumerations](mpi-enumerations.md)

