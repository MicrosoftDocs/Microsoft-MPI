---
title: MPI_Compare_and_swap function
TOCTitle: MPI_Compare_and_swap function
mtps_version: v=VS.85
f1_keywords:
- MPI_COMPARE_AND_SWAP
- mpif/MPI_Compare_and_swap
- mpi/MPI_COMPARE_AND_SWAP
dev_langs:
- C++
- C
description: Learn about the MPI_Compare_and_swap function, its syntax, parameters, and return values. Ideal for users of HPC Pack and MS-MPI Redistributable Package.
---

# MPI\_Compare\_and\_swap function

Performs a remote atomic compare and swap operation. 

## Syntax

``` c++
int MPIAPI MPI_Compare_and_swap(
  _In_  void         *origin_addr,
  _In_  void         *compare_addr,
  _Out_ void         *result_addr,
        MPI_Datatype datatype,
        int          target_rank,
        MPI_Aint     target_disp,
        MPI_Win      win
);
```

## Parameters

  - *origin\_addr* \[in\]  
    initial address of buffer

  - *compare\_addr* \[in\]  
    initial address of comparebuffer

  - *result\_addr* \[out\]  
    initial address of result buffer

  - *datatype*  
    datatype of each entry in all buffers

  - *target\_rank*  
    rank of target

  - *target\_disp*  
    displacement from start of window to beginning of target buffer

  - *win*  
    window object

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMPARE_AND_SWAP(ORIGIN_ADDR, COMPARE_ADDR, RESULT_ADDR,
                DATATYPE, TARGET_RANK, TARGET_DISP, WIN, IERROR)
        <type> ORIGIN_ADDR(*), COMPARE_ADDR(*), RESULT_ADDR(*)
        INTEGER(KIND=MPI_ADDRESS_KIND) TARGET_DISP
        INTEGER DATATYPE, TARGET_RANK, WIN, IERROR
```

## Remarks

This function compares one element of type *datatype* in the compare buffer *compare_addr* with the buffer at offset *target_disp* in the target window specified by *target_rank* and *win* and replaces the value at the target with the value in the origin buffer *origin_addr* if the compare buffer and the target buffer are identical. The original value at the target is returned in the buffer *result_addr*. The parameter datatype must belong to one of the following categories of predefined datatypes: C integer, Fortran integer, Logical, Multi-language types, or Byte. The origin and result buffers (*origin_addr* and *result_addr*) must be disjoint.

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

[MPI One-Sided Communications Functions](mpi-one-sided-communications-functions.md)

