---
title: MPI_Type_create_f90_real function
TOCTitle: MPI_Type_create_f90_real function
ms:assetid: 04ad4925-0708-4733-9453-4e6ee7bcefdc
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473490(v=VS.85)
ms:contentKeyID: 59361025
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_CREATE_F90_REAL
- mpif/MPI_Type_create_f90_real
- mpi/MPI_TYPE_CREATE_F90_REAL
dev_langs:
- C++
- C
---

# MPI\_Type\_create\_f90\_real function

Returns a predefined type that matches the specified range.

## Syntax

``` c++
int MPIAPI MPI_Type_create_f90_real(
        int          p,
        int          r,
  _Out_ MPI_Datatype *newtype
);
```

## Parameters

  - *p*  
    Number of decimal digits in mantissa.

  - *r*  
    Decimal exponent range desired.

  - *newtype* \[out\]  
    A predefine MPI Datatype that matches the range.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_TYPE_CREATE_F90_REAL(P, R, NEWTYPE, IERROR)
        INTEGER P, R, NEWTYPE, IERROR
```

## Remark

This function returns a predefined MPI datatype that matches a REAL variable of *KIND selected\_real\_kind\(p, r\)*. In the model described above it returns a handle for the element *D\(p, r\)*. Either *p* or *r* may be omitted from calls to *selected\_real\_kind\(p, r\)* (but not both). Analogously, either *p* or *r* may be set to **MPI\_UNDEFINED**. In communication, an MPI datatype **A** returned by [**MPI\_Type\_create\_f90\_real**](mpi-type-create-f90-real-function.md) matches a datatype **B** if and only if **B** was returned by [**MPI\_Type\_create\_f90\_real**](mpi-type-create-f90-real-function.md) called with the same values for *p* and *r* or B is a duplicate of such a datatype.

If there is no corresponding type for the specified range, the call is erroneous. This implementation sets *newtype* to **MPI\_DATATYPE\_NULL** and returns an error of class **MPI\_ERR\_ARG**.

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

