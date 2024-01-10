---
title: MPI_Allgatherv function
TOCTitle: MPI_Allgatherv function
ms:assetid: 6f44ceb1-8213-4541-a2d8-639a84a38be2
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn502501(v=VS.85)
ms:contentKeyID: 59360773
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ALLGATHERV
- mpif/MPI_Allgatherv
- mpi/MPI_ALLGATHERV
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Allgatherv
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn how to use the MPI_Allgatherv function in Microsoft's HPC Pack for efficient data distribution among group members. Detailed syntax and parameters explained.
---

# MPI\_Allgatherv function

Gathers a variable amount of data from each member of a group and sends the data to all members of the group. The **MPI\_Allgatherv** function is like the [**MPI\_Gatherv**](mpi-gatherv-function.md), except that all processes receive the result, instead of just the root. The block of data that is sent from the *j*th process is received by every process and placed in the *j*th block of the buffer *recvbuf*. These blocks do not all have to be the same size.

## Syntax

``` c++
int MPIAPI MPI_Allgatherv(
  _In_  void         *sendbuf,
        int          sendcount,
        MPI_Datatype sendtype,
  _Out_ void         *recvbuf,
  _In_  int          *recvcounts,
  _In_  int          *displs,
        MPI_Datatype recvtype,
        MPI_Comm     comm
);
```

## Parameters

  - *sendbuf* \[in\]  
    The pointer to the data to be sent to all processes in the group. The number and data type of the elements in the buffer are specified in the *sendcount* and *sendtype* parameters. Each element in the buffer corresponds to a process in the group.
    
    If the comm parameter references an intracommunicator, you can specify an in-place option by specifying **MPI\_IN\_PLACE** in all processes. The *sendcount* and *sendtype* parameters are ignored. Each process enters data in the corresponding receive buffer element. The *n*th process sends data to the *n*th element of the receive buffer.

  - *sendcount*  
    The number of data elements that this process sends in the buffer that is specified in the *sendbuf* parameter. If an element in *sendcount* is zero, the data part of the message from that process is empty.

  - *sendtype*  
    The MPI data type of the elements in the send buffer.

  - *recvbuf* \[out\]  
    The pointer to a buffer that contains the data that is received from each process. The number and data type of the elements in the buffer are specified in the *recvcount* and *recvtype* parameters.

  - *recvcounts* \[in\]  
    The number of data elements from each communicator process in the receive buffer.

  - *displs* \[in\]  
    The location, relative to the *recvbuf* parameter, of the data from each communicator process.
    
    In the *recvbuf*, *recvcounts*, and *displs* parameter arrays, the *n*th element of each array refers to the data that is received from the *n*th communicator process.

  - *recvtype*  
    The MPI data type of each element in buffer.

  - *comm*  
    The [**MPI\_Comm**](mpi-comm-enumeration.md) communicator handle.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_ALLGATHERV(SENDBUF, SENDCOUNT, SENDTYPE, RECVBUF, RECVCOUNTS,DISPLS, RECVTYPE,COMM, IERROR)
        <type> SENDBUF(*), R.ECVBUF(*)
        INTEGER SENDCOUNT, SENDTYPE, RECVCOUNTS(*), DISPLS(*), RECVTYPE, COMM, IERROR
```

## Remarks

The usage rules for **MPI\_Allgatherv** correspond to the rules for [**MPI\_Gatherv**](mpi-gatherv-function.md).

The type signature that is associated with the *sendtype* parameter on a process must be equal to the type signature that is associated with the *recvtype* parameter on any other process.

If the *comm* parameter references an intracommunicator, the outcome of a call to `MPI_Allgatherv(...)`is as if all processes executed calls to `MPI_GatherV(sendbuf,sendcount,sendtype,recvbuf,recvcounts,displs,recvtype,root,comm)`, for `root = 0 , ..., n-1`.

If the *comm* parameter references an intercommunicator, then each process of one group, for example, group A, contributes the number of data items that are specified in the *sendcount* parameter. This data is concatenated, and the result is stored at each process in the other group, group B. Conversely, the concatenation of the data of the processes in group B is stored at each process in group A. The send buffer parameters in group A must be consistent with the receive buffer parameters in group B, and vice versa.

## Requirements

<table>
<colgroup>
<col/>
<col/>
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

[**MPI\_Gatherv**](mpi-gatherv-function.md)

[**MPI\_Datatype**](mpi-datatype-enumeration.md)

