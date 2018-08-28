---
title: MPI_Scan function
TOCTitle: MPI_Scan function
ms:assetid: d7d4782a-6140-4696-99a8-849efb219ea8
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473464(v=VS.85)
ms:contentKeyID: 59360999
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_SCAN
- mpif/MPI_Scan
- mpi/MPI_SCAN
dev_langs:
- C++
- C
---

# MPI\_Scan function

TBD

## Syntax

``` c++
int MPIAPI MPI_Scan(
  _In_  void         *sendbuf,
  _Out_ void         *recvbuf,
        int          count,
        MPI_Datatype datatype,
        MPI_Op       op,
        MPI_Comm     comm
);
```

## Parameters

  - *sendbuf* \[in\]  
    TBD

  - *recvbuf* \[out\]  
    TBD

  - *count*  
    TBD

  - *datatype*  
    TBD

  - *op*  
    TBD

  - *comm*  
    TBD

## Return value

TBD

## Fortran

    MPI_SCAN(SENDBUF, RECVBUF, COUNT, DATATYPE, OP, COMM, IERROR)
        <type> SENDBUF(*), RECVBUF(*)
        INTEGER COUNT, DATATYPE, OP, COMM, IERROR

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

[MPI Collective Functions](mpi-collective-functions.md)

