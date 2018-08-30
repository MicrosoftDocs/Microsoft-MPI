---
title: MPI_Attr_put function
TOCTitle: MPI_Attr_put function
ms:assetid: d58fed6e-4489-4082-a059-361dd2833414
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473235(v=VS.85)
ms:contentKeyID: 59360781
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ATTR_PUT
- mpif/MPI_Attr_put
- mpi/MPI_ATTR_PUT
dev_langs:
- C++
- C
---

# MPI\_Attr\_put function

This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Comm\_set\_attr**](mpi-comm-set-attr-function.md) function.

## Syntax

``` c++
int
MPIAPI MPI_Attr_put(
       MPI_Comm comm,
       int      keyval,
  _In_ void     *attribute_val
);
```

## Parameters

  - *comm*  
    Communicator to which attribute will be attached.

  - *keyval*  
    Key value, as returned by MPI_KEYVAL_CREATE.

  - *attribute\_val* \[in\]  
    Attribute value.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_ATTR_PUT(COMM, KEYVAL, ATTRIBUTE_VAL, IERROR)
        INTEGER COMM, KEYVAL, ATTRIBUTE_VAL, IERROR

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

[**MPI\_Comm\_set\_attr**](mpi-comm-set-attr-function.md)

