---
title: MPI_Comm_copy_attr_function function
TOCTitle: MPI_Comm_copy_attr_function function
ms:assetid: fc983377-ed92-4f7e-b50d-06283c14eb6d
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473260(v=VS.85)
ms:contentKeyID: 59360806
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- COMM_COPY_ATTR_FUNCTION
- mpi/COMM_COPY_ATTR_FUNCTION
- mpi/MPI_Comm_copy_attr_function
- MPI_Comm_copy_attr_function
- mpif/COMM_COPY_ATTR_FUNCTION
- mpif/MPI_Comm_copy_attr_function
dev_langs:
- C++
- C
description: Master the MPI_Comm_Copy_Attr_Function for efficient message-passing in Microsoft HPC Pack. Enhance communicator duplication & attribute management.
---

# MPI\_Comm\_copy\_attr\_function function

**MPI\_Comm\_copy\_attr\_function** is a placeholder for the application-defined function name.

## Syntax

``` c++
int MPI_Comm_copy_attr_function(
           MPI_Comm oldcomm,
           int      comm_keyval,
  _In_opt_ void     *extra_state,
  _In_     void     *attribute_val_in,
  _Out_    void     *attribute_val_out,
  _Out_    int      *flag
);
```

## Parameters

  - *oldcomm*  
    Original communicator.

  - *comm\_keyval*  
    Key value.

  - *extra\_state* \[in, optional\]  
    Extra state.

  - *attribute\_val\_in* \[in\]  
    Source attribute value.

  - *attribute\_val\_out* \[out\]  
    Destination attribute value.

  - *flag* \[out\]  
    If the returned value of *flag* is 0 or **FALSE**, then the attribute is deleted in the duplicated communicator. Otherwise (*flag* = 1 or **TRUE**), the new attribute value is set to the value returned in *attribute\_val\_out*.

## Return value

The function returns **MPI\_SUCCESS** on success and an error code on failure.

## Fortran

``` FORTRAN
    SUBROUTINE COMM_COPY_ATTR_FUNCTION(OLDCOMM, COMM_KEYVAL, EXTRA_STATE,
                ATTRIBUTE_VAL_IN, ATTRIBUTE_VAL_OUT, FLAG, IERROR)
        INTEGER OLDCOMM, COMM_KEYVAL, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) EXTRA_STATE, ATTRIBUTE_VAL_IN,
            ATTRIBUTE_VAL_OUT
        LOGICAL FLAG
```

## Remarks

The *comm\_copy\_attr\_fn* function is invoked when a communicator is duplicated by [**MPI\_Comm\_dup**](mpi-comm-dup-function.md).

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

[**MPI\_Comm\_create\_keyval**](mpi-comm-create-keyval-function.md)

