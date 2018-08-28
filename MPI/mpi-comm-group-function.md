---
title: MPI_Comm_group function
TOCTitle: MPI_Comm_group function
ms:assetid: 45ad9c9c-1a68-4837-827e-992355639b3d
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473275(v=VS.85)
ms:contentKeyID: 59360821
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_GROUP
- mpif/MPI_Comm_group
- mpi/MPI_COMM_GROUP
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Comm_group
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

# MPI\_Comm\_group function

Retrieves the group that is associated with a communicator.

## Syntax

``` c++
int MPIAPI MPI_Comm_group(
        MPI_Comm  comm,
  _Out_ MPI_Group *group
);
```

## Parameters

  - *comm*  
    The communicator on which to base the group.

  - *group* \[out\]  
    On return, contains the handle to the group that is associated with the specified communicator.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_COMM_GROUP(COMM, GROUP, IERROR)
        INTEGER COMM, GROUP, IERROR

## Remarks

This is a local operation. Different processes can define distinct groups. A process can define a group that does not include itself.

The MPI implementation does not provide a mechanism to build a group from scratch, but only from existing groups. The base group, on which all other groups are defined, is the group that is associated with the initial communicator **MPI\_COMM\_WORLD**.

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

