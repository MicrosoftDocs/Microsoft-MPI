---
title: MPI_Recv function
TOCTitle: MPI_Recv function
ms:assetid: 3268d295-b055-4960-bee4-6ba9dbe50904
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473453(v=VS.85)
ms:contentKeyID: 59360988
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_RECV
- mpif/MPI_Recv
- mpi/MPI_RECV
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Recv
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn about the MPI_Recv function on Microsoft's official site. Understand its syntax, parameters, return values, and how it performs a receive operation.
---

# MPI\_Recv function

Performs a receive operation and does not return until a matching message is received.

## Syntax

``` c++
int MPIAPI MPI_Recv(
  _In_opt_ void         *buf,
           int          count,
           MPI_Datatype datatype,
           int          source,
           int          tag,
           MPI_Comm     comm,
  _Out_    MPI_Status   *status
);
```

## Parameters

  - *buf* \[in, optional\]  
    A pointer to the buffer that contains the data to be sent.

  - *count*  
    The number of elements in the buffer. If the data part of the message is empty, set the *count* parameter to 0.

  - *datatype*  
    The data type of the elements in the buffer array.

  - *source*  
    The rank of the sending process within the specified communicator. Specify the **MPI\_ANY\_SOURCE** constant to specify that any source is acceptable.

  - *tag*  
    The message tag that is used to distinguish different types of messages. Specify the **MPI\_ANY\_TAG** constant to indicate that any tag is acceptable.

  - *comm*  
    The handle to the communicator.

  - *status* \[out\]  
    On return, contains a pointer to an [**MPI\_Status**](mpi-status-structure.md) structure where information about the received message is stored.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_RECV(BUF, COUNT, DATATYPE, SOURCE, TAG, COMM, STATUS, IERROR)
        <type> BUF(*)
        INTEGER COUNT, DATATYPE, SOURCE, TAG, COMM, STATUS(MPI_STATUS_SIZE), IERROR
```

## Remarks

The length of the received message must be less than or equal to the length of the receive buffer. This function returns an overflow error if all incoming data does not fit into the receive buffer.

If the received message is shorter than the buffer, only the part of the buffer that corresponds to the message is modified. The remainder of the buffer is not modified.

Processes can send messages to themselves. However, it is unsafe to do so with the blocking send and receive operations, [**MPI\_Send**](mpi-send-function.md) and **MPI\_Recv**, because these blocking send and receive operations can cause a deadlock.

> [!NOTE]
> There is an asymmetry between send and receive operations. A receive operation can accept messages from an arbitrary sender, but a send operation must specify a unique receiver. This implements a push style of communication, where data transfer is effected by the sender, rather than a pull style where data transfer is effected by the receiver.

 

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

[MPI Point to Point Functions](mpi-point-to-point-functions.md)

[**MPI\_Send**](mpi-send-function.md)

[**MPI\_Irecv**](mpi-irecv-function.md)

[**MPI\_Datatype**](mpi-datatype-enumeration.md)

[**MPI\_Comm**](mpi-comm-enumeration.md)

[**MPI\_Status**](mpi-status-structure.md)

