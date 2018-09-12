---
title: MPI_Mrecv function
TOCTitle: MPI_Mrecv function
ms:assetid: C31BC7F5-80CD-42FE-9BF9-E6D81A1231C4
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn985833(v=VS.85)
ms:contentKeyID: 65288037
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_MRECV
- mpif/MPI_Mrecv
- mpi/MPI_MRECV
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Mrecv
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

# MPI\_Mrecv function

Performs a blocking receive for a message matched by [**MPI\_Mprobe**](mpi-mprobe-function.md) or [**MPI\_Improbe**](mpi-improbe-function.md).

## Syntax

``` c++
int MPIAPI MPI_Mrecv(
  _Out_   void         *buf,
  _In_    int          count,
  _In_    MPI_Datatype datatype,
  _Inout_ MPI_Message  *message,
  _Out_   MPI_Status   *status
);
```

## Parameters

  - *buf* \[out\]  
    A pointer to the address of the receive buffer.

  - *count* \[in\]  
    The number of *datatype* elements in *buf*.

  - *datatype* \[in\]  
    The MPI data type of the elements in the buffer array.

  - *message* \[in, out\]  
    Contains a pointer to the message.

  - *status* \[out\]  
    On return, contains a pointer to an [**MPI\_Status**](mpi-status-structure.md) structure where information about the message is stored.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_MRECV(BUF, COUNT, DATATYPE, MESSAGE, STATUS, IERROR)
        <type> BUF(*)
        INTEGER COUNT, DATATYPE, MESSAGE, STATUS(MPI_STATUS_SIZE), IERROR
```

## Remarks

This function receives a message matched by a matching probe operation. The receive buﬀer consists of the storage containing *count* consecutive elements of the type speciﬁed by *datatype*, starting at address *buf*. The length of the received message must be less than or equal to the length of the receive buﬀer. An overﬂow error occurs if all incoming data does not ﬁt, without truncation, into the receive buﬀer.

If the message is shorter than the receive buﬀer, then only those locations corresponding to the (shorter) message are modiﬁed.

On return from this function, the message handle is set to **MPI\_MESSAGE\_NULL**. All errors that occur during the execution of this operation are handled according to the error handler set for the communicator used in the matching probe call that produced the message handle

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

[**MPI\_Mprobe**](mpi-mprobe-function.md)

[**MPI\_Improbe**](mpi-improbe-function.md)

[**MPI\_Recv**](mpi-recv-function.md)

[**MPI\_Imrecv**](mpi-imrecv-function.md)

