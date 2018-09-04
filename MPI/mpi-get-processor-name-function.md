---
title: MPI_Get_processor_name function
TOCTitle: MPI_Get_processor_name function
ms:assetid: cdbe3718-c1f5-4c6c-a34a-2263c76ee30d
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473382(v=VS.85)
ms:contentKeyID: 59360918
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GET_PROCESSOR_NAME
- mpif/MPI_Get_processor_name
- mpi/MPI_GET_PROCESSOR_NAME
dev_langs:
- C++
- C
---

# MPI\_Get\_processor\_name function

Gets the name of the processor.

## Syntax

``` c++
int MPIAPI MPI_Get_processor_name(
        _Out_z_cap_post_count_(MPI_MAX_PROCESSOR_NAME,*resultlen) char *name,
  _Out_ int                                                            *resultlen
);
```

## Parameters

  - *name*  
    A unique specifier for the actual (as opposed to virtual) node. This must be an array of size at least **MPI\_MAX\_PROCESSOR\_NAME**.

  - *resultlen* \[out\]  
    Length (in characters) of the name.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_GET_PROCESSOR_NAME( NAME, RESULTLEN, IERROR)
        CHARACTER*(*) NAME
        INTEGER RESULTLEN,IERROR

## Remarks

  The name returned should identify a particular piece of hardware; the exact format is implementation defined.  This name may or may not be the same as might be returned by 'gethostname', 'uname', or 'sysinfo'.

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

[MPI Management Functions](mpi-management-functions.md)

