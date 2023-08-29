---
title: MPI_Gather function
TOCTitle: MPI_Gather function
ms:assetid: 16b5a535-42c9-4471-a8ef-c1458ea3b261
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473376(v=VS.85)
ms:contentKeyID: 59360912
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GATHER
- mpif/MPI_Gather
- mpi/MPI_GATHER
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Gather
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: "Master MPI Gather Function: Efficiently gather data from group members at Learn Microsoft. Boost your parallel computing skills."
---

# MPI\_Gather function

Gathers data from all members of a group to one member.

## Syntax

``` c++
int MPIAPI MPI_Gather(
  _In_      void         *sendbuf,
            int          sendcount,
            MPI_Datatype sendtype,
  _Out_opt_ void         *recvbuf,
            int          recvcount,
            MPI_Datatype recvtype,
            int          root,
            MPI_Comm     comm
);
```

## Parameters

  - *sendbuf* \[in\]  
    The pointer to a buffer that contains the data to be sent to the root process.
    
    If the *comm* parameter references an intracommunicator, you can specify an in-place option by specifying **MPI\_IN\_PLACE** in all processes. The *sendcount* and *sendtype* parameters are ignored. Each process enters data in the corresponding receive buffer element. The *n*th process sends data to the *n*th element of the receive buffer. The data that is sent by the root process is assumed to be in the correct place in the receive buffer.

  - *sendcount*  
    The number of elements in the send buffer. If *sendcount* is zero, the data part of the message is empty.

  - *sendtype*  
    The data type of each element in the buffer.

  - *recvbuf* \[out, optional\]  
    The pointer to a buffer on the root process that contains the data that is received from each process. It includes data that is sent by the root process. This parameter is significant only at the root process. The *recvbuf* parameter is ignored for all non-root processes.

  - *recvcount*  
    The number of elements that are received from each process. This number is not the total number of items in the buffer. If the count is zero, the data part of the message is empty. This parameter is significant only at the root process.

  - *recvtype*  
    The MPI data type of each element in buffer. This parameter is significant only at the root process.

  - *root*  
    The rank of the receiving process within the specified communicator.

  - *comm*  
    The [**MPI\_Comm**](mpi-comm-enumeration.md) communicator handle.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_GATHER(SENDBUF, SENDCOUNT, SENDTYPE, RECVBUF, RECVCOUNT, RECVTYPE, ROOT, COMM, IERROR)
        <type> SENDBUF(*), RECVBUF(*)
        INTEGER SENDCOUNT, SENDTYPE, RECVCOUNT, RECVTYPE, ROOT, COMM, IERROR
```

## Remarks

All the function parameters are significant on the root process, only the *sendbuf*, *sendcount*, *sendtype*, *root*, and *comm* are significant on the other processes. The *root* and *comm* parameters must be identical on all processes.

Generally, derived data types are allowed for both the *sendtype* and *recvtype* parameters. The type signature that is specified by the *sendtype* and *recvtype* parameters on each process must be equal to the type signature of the *recvcount* and *sendcount* parameters on the root process. The amount of data that is sent must be equal to the amount of data that is received between the root process and each individual process. Distinct type maps between sender and receiver are still allowed.

The specification of counts and types should not cause any location on the root to be written more than one time. Such a call is erroneous.

If the *comm* parameter references an intracommunicator, all processes send the contents of its send buffer to the root process. The root process receives the messages and stores them in rank order. The outcome is as if each of the *n* processes in the group executed a call to `MPI_Send(sendbuf, sendcount, sendtype, root, …)`; and the root had executed *n* calls to `MPI_Recv(recvbuf + i*recvcount*extent(recvtype), recvcount, recvtype, i, …)`. The value of `extent(recvtype)` is obtained by using the [**MPI\_Type\_get\_extent**](mpi-type-get-extent-function.md) function. An alternative description of the function is that the *n* messages that are sent by the processes in the group are concatenated in rank order, and the resulting message is received by the root as if by a call to `MPI_RECV(recvbuf, recvcountn, recvtype, ...)`. The receive buffer is ignored for all non-root processes.

If the *comm* parameter references an intercommunicator, then the call involves all processes in the intercommunicator, but with one group, group A, that defines the root process. All processes in the other group, group B, set the same value in *root* parameter, that is, the rank of the root process in group A. The root process sets the value **MPI\_ROOT** in the *root* parameter. All other processes in group A set the value **MPI\_PROC\_NULL** in the *root* parameter. Data is broadcast from the root process to all processes in group B. The *buffer* parameters of the processes in group B must be consistent with the *buffer* parameter of the root process.

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

[**MPI\_Datatype**](mpi-datatype-enumeration.md)

[**MPI\_Gatherv**](mpi-gatherv-function.md)

