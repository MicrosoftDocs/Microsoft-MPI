---
title: MPI_Group_translate_ranks function
TOCTitle: MPI_Group_translate_ranks function
ms:assetid: 3c93c90e-2c99-4e37-8662-c7adea21f291
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473406(v=VS.85)
ms:contentKeyID: 59360942
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GROUP_TRANSLATE_RANKS
- mpif/MPI_Group_translate_ranks
- mpi/MPI_GROUP_TRANSLATE_RANKS
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Group_translate_ranks
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

# MPI\_Group\_translate\_ranks function

Determines the relative numbering of the same processes in two different groups.

## Syntax

``` c++
int MPIAPI MPI_Group_translate_ranks(
        MPI_Group         group1,
        int               n,
        _In_count_(n) int *ranks1,
        MPI_Group         group2,
  _Out_ int               *ranks2
);
```

## Parameters

  - *group1*  
    The first group.

  - *n*  
    The number or ranks in the *ranks1* and *ranks2* parameter arrays.

  - *ranks1*  
    Zero or more valid ranks in the first group.
    
    > [!NOTE]
    > The **MPI\_PROC\_NULL** constant is valid for this parameter. The corresponding rank that is returned in the *ranks2* parameter is also **MPI\_PROC\_NULL**.
    
     

  - *group2*  
    The second group.

  - *ranks2* \[out\]  
    On return, points to the corresponding ranks in the second group. The value **MPI\_UNDEFINED** indicates that a process is in the first group, but not the second.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_GROUP_TRANSLATE_RANKS( GROUP1, N, RANKS1, GROUP2, RANKS2, IERROR)
        INTEGER GROUP1, N, RANKS1(*), GROUP2, RANKS2(*), IERROR

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

[**MPI\_Group\_incl**](mpi-group-incl-function.md)

