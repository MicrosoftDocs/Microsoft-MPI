---
title: MPI_Group_rank function
TOCTitle: MPI_Group_rank function
ms:assetid: 34650411-2dd1-447c-bca0-6122f43234cb
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473404(v=VS.85)
ms:contentKeyID: 59360940
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GROUP_RANK
- mpif/MPI_Group_rank
- mpi/MPI_GROUP_RANK
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Group_rank
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

# MPI\_Group\_rank function

Returns the rank of the calling process in the specified group.

## Syntax

``` c++
int MPIAPI MPI_Group_rank(
        MPI_Group group,
  _Out_ int       *rank
);
```

## Parameters

  - *group*  
    Specifies the group to query.

  - *rank* \[out\]  
    A pointer to an integer that, on return, contains the rank of the calling process in the specified group. A value of **MPI\_UNDEFINED** that the calling process is not a member of the specified group.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_GROUP_RANK(GROUP, RANK, IERROR)
        INTEGER GROUP, RANK, IERROR 

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

[MPI Group Functions](mpi-group-functions.md)

