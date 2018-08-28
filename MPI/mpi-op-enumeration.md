---
title: MPI_Op enumeration
TOCTitle: MPI_Op enumeration
ms:assetid: 3C70A7BA-E67A-434F-BF13-F42F498B8150
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473436(v=VS.85)
ms:contentKeyID: 59360972
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_BAND
- mpi/MPI_BOR
- mpi/MPI_BXOR
- mpi/MPI_LAND
- mpi/MPI_LOR
- mpi/MPI_LXOR
- mpi/MPI_MAX
- mpi/MPI_MAXLOC
- mpi/MPI_MIN
- mpi/MPI_MINLOC
- mpi/MPI_Op
- mpi/MPI_OP_NULL
- mpi/MPI_PROD
- mpi/MPI_REPLACE
- mpi/MPI_SUM
- MPI_BAND
- MPI_BOR
- MPI_BXOR
- MPI_LAND
- MPI_LOR
- MPI_LXOR
- MPI_MAX
- MPI_MAXLOC
- MPI_MIN
- MPI_MINLOC
- MPI_Op
- MPI_OP_NULL
- MPI_PROD
- MPI_REPLACE
- MPI_SUM
dev_langs:
- C++
- C
api_location:
- mpi.h
api_name:
- MPI_Op
api_type:
- HeaderDef
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
---

# MPI\_Op enumeration

TBD

## Syntax

``` c++
typedef enum _MPI_Op { 
  MPI_OP_NULL  = 0x18000000,
  MPI_MAX      = 0x58000001,
  MPI_MIN      = 0x58000003,
  MPI_SUM      = 0x58000003,
  MPI_PROD     = 0x58000004,
  MPI_LAND     = 0x58000005,
  MPI_BAND     = 0x58000006,
  MPI_LOR      = 0x58000007,
  MPI_BOR      = 0x58000008,
  MPI_LXOR     = 0x58000009,
  MPI_BXOR     = 0x5800000a,
  MPI_MINLOC   = 0x5800000b,
  MPI_MAXLOC   = 0x5800000c,
  MPI_REPLACE  = 0x5800000d
} MPI_Op;
```

## Constants

  - **MPI\_OP\_NULL**

  - **MPI\_MAX**

  - **MPI\_MIN**

  - **MPI\_SUM**

  - **MPI\_PROD**

  - **MPI\_LAND**

  - **MPI\_BAND**

  - **MPI\_LOR**

  - **MPI\_BOR**

  - **MPI\_LXOR**

  - **MPI\_BXOR**

  - **MPI\_MINLOC**

  - **MPI\_MAXLOC**

  - **MPI\_REPLACE**

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

