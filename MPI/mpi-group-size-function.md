---
title: MPI_Group_size function
TOCTitle: MPI_Group_size function
ms:assetid: a946e817-a999-4ded-8465-9a52a7ce8783
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473405(v=VS.85)
ms:contentKeyID: 59360941
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GROUP_SIZE
- mpif/MPI_Group_size
- mpi/MPI_GROUP_SIZE
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Group_size
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
---

# MPI\_Group\_size function

Retrieves the size of the specified group.

## Syntax

``` c++
int MPIAPI MPI_Group_size(
        MPI_Group group,
  _Out_ int       *size
);
```

## Parameters

  - *group*  
    The group to evaluate.

  - *size* \[out\]  
    A pointer to an integer that, on return, contains the size of the specified group.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_GROUP_SIZE(GROUP, SIZE, IERROR)
        INTEGER GROUP, SIZE, IERROR 
```

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

[MPI Group Functions](mpi-group-functions.md)

