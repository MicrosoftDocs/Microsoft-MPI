---
title: MPI_Comm_get_attr function
TOCTitle: MPI_Comm_get_attr function
ms:assetid: 7fa4c249-273c-40a3-9dfb-2dd754adb259
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473271(v=VS.85)
ms:contentKeyID: 59360817
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_GET_ATTR
- mpif/MPI_Comm_get_attr
- mpi/MPI_COMM_GET_ATTR
dev_langs:
- C++
- C
---

# MPI\_Comm\_get\_attr function

TBD

## Syntax

``` c++
int MPIAPI MPI_Comm_get_attr(
        MPI_Comm comm,
        int      comm_keyval,
  _Out_ void     *attribute_val,
  _Out_ int      *flag
);
```

## Parameters

  - *comm*  
    TBD

  - *comm\_keyval*  
    TBD

  - *attribute\_val* \[out\]  
    TBD

  - *flag* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_COMM_GET_ATTR(COMM, COMM_KEYVAL, ATTRIBUTE_VAL, FLAG, IERROR)
        INTEGER COMM, COMM_KEYVAL, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) ATTRIBUTE_VAL
        LOGICAL FLAG

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

[MPI Caching Functions](mpi-caching-functions.md)

