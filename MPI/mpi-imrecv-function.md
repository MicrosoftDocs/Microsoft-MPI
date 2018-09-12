---
title: MPI_Imrecv function
TOCTitle: MPI_Imrecv function
ms:assetid: E91DF5CA-9A31-4D30-B9CC-44AD4BEFF6C2
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn985830(v=VS.85)
ms:contentKeyID: 65288034
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_IMRECV
- mpif/MPI_Imrecv
- mpi/MPI_IMRECV
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Imrecv
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

# MPI\_Imrecv function

Performs a non-blocking receive for a message matched by [**MPI\_Mprobe**](mpi-mprobe-function.md) or [**MPI\_Improbe**](mpi-improbe-function.md).

## Syntax

``` c++
int MPIAPI MPI_Imrecv(
  _Out_   void         *buf,
  _In_    int          count,
  _In_    MPI_Datatype datatype,
  _Inout_ MPI_Message  *message,
  _Out_   MPI_Request  *request
);
```

## Parameters

  - *buf* \[out\]  
    A pointer to the address of the receive buffer.

  - *count* \[in\]  
    The number of *datatype* elements in *buf*.

  - *datatype* \[in\]  
    The MPI data type of the elements in *buf*.

  - *message* \[in, out\]  
    Contains a pointer to the message.

  - *request* \[out\]  
    On return, contains a pointer to an **MPI\_REQUEST** handle representing the communication operation.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_IMRECV(BUF, COUNT, DATATYPE, MESSAGE, REQUEST, IERROR)
        <type> BUF(*)
        INTEGER COUNT, DATATYPE, MESSAGE, REQUEST, IERROR
```

## Remarks

This function is the non-blocking variant of [**MPI\_Mrecv**](mpi-mrecv-function.md) and starts a non-blocking receive of a matched message. Completion semantics are similar to [**MPI\_Irecv**](mpi-irecv-function.md).

On return from this function, the message handle is set to **MPI\_MESSAGE\_NULL**.

If this function is called with **MPI\_MESSAGE\_NO\_PROC** as the message argument, the call returns immediately with a request object which, when completed, will yield a status object set to *source* = **MPI\_PROC\_NULL**, *tag* = **MPI\_ANY\_TAG**, and *count* = 0, as if a receive from **MPI\_PROC\_NULL** was issued. A call to this function with **MPI\_MESSAGE\_NULL** is erroneous.

## Requirements

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Product</p></td>
<td><p>Microsoft MPI v6</p></td>
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

[MPI Point to Point Functions](mpi-point-to-point-functions.md)

[**MPI\_Irecv**](mpi-irecv-function.md)

[**MPI\_Mrecv**](mpi-mrecv-function.md)

[**MPI\_Mprobe**](mpi-mprobe-function.md)

[**MPI\_Improbe**](mpi-improbe-function.md)

