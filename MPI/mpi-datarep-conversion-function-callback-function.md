---
title: MPI_Datarep_conversion_function callback function
TOCTitle: MPI_Datarep_conversion_function callback function
ms:assetid: e8271935-4647-4436-9a4a-7d7ce2e573c3
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473288(v=VS.85)
ms:contentKeyID: 59360834
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- DATAREP_CONVERSION_FUNCTION
- mpi/DATAREP_CONVERSION_FUNCTION
- mpi/MPI_Datarep_conversion_function
- MPI_Datarep_conversion_function
- mpif/DATAREP_CONVERSION_FUNCTION
- mpif/MPI_Datarep_conversion_function
dev_langs:
- C++
- C
---

# MPI\_Datarep\_conversion\_function callback function

This function is a place holder for the user-defind functions to converts from file data representation to native representation and vice versa. 

## Syntax

``` c++
int MPI_Datarep_conversion_function(
       _Inout_ void *userbuf,
       MPI_Datatype datatype,
       int          count,
       _Inout_ void *filebuf,
       MPI_Offset   position,
  _In_ void         *extra_state
);
```

## Parameters

  - *userbuf*  
    Native buffer.

  - *datatype*  
    Datatype of the elements.

  - *count*  
    Number of elements.

  - *filebuf*  
    File buffer.

  - *position*  
    Position in the read buffer.

  - *extra\_state* \[in\]  
    Extra state.

## Return value

The conversion functions should return an error code. If the returned error code has a value other than **MPI\_SUCCESS**, the implementation will raise an error in the class **MPI\_ERR\_CONVERSION**.

## Fortran

``` FORTRAN
    SUBROUTINE DATAREP_CONVERSION_FUNCTION(USERBUF, DATATYPE, COUNT, FILEBUF,
                POSITION, EXTRA_STATE, IERROR)
        <TYPE> USERBUF(*), FILEBUF(*)
        INTEGER COUNT, DATATYPE, IERROR
        INTEGER(KIND=MPI_OFFSET_KIND) POSITION
        INTEGER(KIND=MPI_ADDRESS_KIND) EXTRA_STATE
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
</tbody>
</table>


## See also

[MPI Miscellaneous Functions](mpi-miscellaneous-functions.md)

[**MPI\_Register\_datarep**](mpi-register-datarep-function.md)

