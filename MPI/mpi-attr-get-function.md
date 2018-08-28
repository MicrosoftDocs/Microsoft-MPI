---
title: MPI_Attr_get function
TOCTitle: MPI_Attr_get function
ms:assetid: f428b242-2f49-4d01-abf5-12af7e5a487c
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473234(v=VS.85)
ms:contentKeyID: 59360780
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ATTR_GET
- mpif/MPI_Attr_get
- mpi/MPI_ATTR_GET
dev_langs:
- C++
- C
---

# MPI\_Attr\_get function

This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Comm\_get\_attr**](mpi-comm-get-attr-function.md) function.

## Syntax

``` c++
int
MPIAPI MPI_Attr_get(
        MPI_Comm comm,
        int      keyval,
  _Out_ void     *attribute_val,
  _Out_ int      *flag
);
```

## Parameters

  - *comm*  
    TBD

  - *keyval*  
    TBD

  - *attribute\_val* \[out\]  
    TBD

  - *flag* \[out\]  
    TBD

## Return value

TBD

## Fortran

    MPI_ATTR_GET(COMM, KEYVAL, ATTRIBUTE_VAL, FLAG, IERROR)
        INTEGER COMM, KEYVAL, ATTRIBUTE_VAL, IERROR
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

[MPI Miscellaneous Functions](mpi-miscellaneous-functions.md)

[**MPI\_Comm\_get\_attr**](mpi-comm-get-attr-function.md)

