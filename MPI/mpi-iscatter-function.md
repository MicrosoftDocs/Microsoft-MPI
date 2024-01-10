---
title: MPI_Iscatter function
TOCTitle: MPI_Iscatter function
ms:assetid: 17138DD8-9BBF-45F2-A31B-252B90EBD0C8
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Mt629169(v=VS.85)
ms:contentKeyID: 71965705
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ISCATTER
- mpif/MPI_Iscatter
- mpi/MPI_ISCATTER
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Iscatter
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Master the MPI_Iscatter function with our comprehensive guide. Learn how to scatter data across all group members in a non-blocking way with Microsoft MPI.
---

# MPI\_Iscatter function

Scatters data from one member across all members of a group in a non-blocking way. This function performs the inverse of the operation that is performed by the [**MPI\_Igather**](mpi-igather-function.md)function.

## Syntax

``` c++
int MPIAPI MPI_Iscatter(
  _In_opt_  const void         *sendbuf,
  _In_             int         sendcount,
  _In_            MPI_Datatype sendtype,
  _Out_opt_       void         *recvbuf,
  _In_            int          recvcount,
  _In_            MPI_Datatype recvtype,
  _In_            int          root,
  _In_            MPI_Comm     comm,
  _Out_           MPI_Request  *request
);
```

## Parameters

  - *sendbuf* \[in, optional\]  
    The pointer to a buffer that contains the data to be sent to the root process.
    
    This parameter is ignored for all non-root processes.
    
    If the *comm* parameter references an intracommunicator, you can specify an in-place option by specifying **MPI\_IN\_PLACE** in the root process. The *recvcount* and *recvtype* parameters are ignored. The scattered vector is still considered to contain *n* segments, where *n* is the group size; the segment that corresponds to the root process is not moved.

  - *sendcount* \[in\]  
    The number of elements in the send buffer. If *sendcount* is zero, the data part of the message is empty.
    
    This parameter is ignored for all non-root processes.

  - *sendtype* \[in\]  
    The data type of each element in the buffer.
    
    This parameter is ignored for all non-root processes.

  - *recvbuf* \[out, optional\]  
    The handle to a buffer that contains the data that is received on each process. The number and data type of the elements in the buffer are specified in the *recvcount* and *recvtype* parameters.

  - *recvcount* \[in\]  
    The number of elements in the receive buffer. If the count is zero, the data part of the message is empty.

  - *recvtype* \[in\]  
    The MPI data type of the elements in the receive buffer.

  - *root* \[in\]  
    The rank of the receiving process within the specified communicator.

  - *comm* \[in\]  
    The [**MPI\_Comm**](mpi-comm-enumeration.md) communicator handle.

  - *request* \[out\]  
    The [**MPI\_Request**](mpi-comm-enumeration.md) handle representing the communication operation.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_ISCATTER(SENDBUF, SENDCOUNT, SENDTYPE, RECVBUF, RECVCOUNT, RECVTYPE, ROOT, COMM, REQUEST, IERROR)
        <type> SENDBUF(*), RECVBUF(*)
        INTEGER SENDCOUNT, SENDTYPE, RECVCOUNT, RECVTYPE, ROOT, COMM, REQUEST, IERROR
```

## Remarks

A non-blocking call initiates a collective reduction operation which must be completed in a separate completion call. Once initiated, the operation may progress independently of any computation or other communication at participating processes. In this manner, non-blocking reduction operations can mitigate possible synchronizing eﬀects of reduction operations by running them in the “background.”

All completion calls (e.g., [**MPI\_Wait)**](mpi-wait-function.md) are supported for non-blocking reduction operations.

## Requirements

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Product</p></td>
<td><p>Microsoft MPI v7</p></td>
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

[**MPI\_Datatype**](mpi-datatype-enumeration.md)

[**MPI\_Scatter**](mpi-scatter-function.md)

[**MPI\_Test**](mpi-test-function.md)

[**MPI\_Testall**](mpi-testall-function.md)

[**MPI\_Testany**](mpi-testany-function.md)

[**MPI\_Testsome**](mpi-testsome-function.md)

[**MPI\_Wait**](mpi-wait-function.md)

[**MPI\_Waitall**](mpi-waitall-function.md)

[**MPI\_Waitany**](mpi-waitany-function.md)

[**MPI\_Waitsome**](mpi-waitsome-function.md)

