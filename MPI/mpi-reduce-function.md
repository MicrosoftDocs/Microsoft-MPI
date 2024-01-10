---
title: MPI_Reduce function
TOCTitle: MPI_Reduce function
ms:assetid: 2b048e6f-e398-4910-95b3-08b8933f696a
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473455(v=VS.85)
ms:contentKeyID: 59360990
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_REDUCE
- mpif/MPI_Reduce
- mpi/MPI_REDUCE
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Reduce
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Master the MPI_Reduce Function for efficient global operations across groups with Microsoft's Message Passing Interface. Learn more now.
---

# MPI\_Reduce function

Performs a global reduce operation across all members of a group. You can specify a predefined mathematical or logical operation or an application-defined operation.

## Syntax

``` c++
int MPIAPI MPI_Reduce(
  _In_      void         *sendbuf,
  _Out_opt_ void         *recvbuf,
            int          count,
            MPI_Datatype datatype,
            MPI_Op       op,
            int          root,
            MPI_Comm     comm
);
```

## Parameters

  - *sendbuf* \[in\]  
    The handle to a buffer that contains the data to be sent to the root process.
    
    If the comm parameter references an intracommunicator, you can specify an in place option by specifying **MPI\_IN\_PLACE** in all processes. The *sendcount* and *sendtype* parameters are ignored. Each process enters data in the corresponding receive buffer element. The *n*th process sends data to the *n*th element of the receive buffer. The root process takes its input data from the corresponding element of the receive buffer and replaces it with the output data.

  - *recvbuf* \[out, optional\]  
    The handle to a buffer to receive the result of the reduction operation. This parameter is significant only at the root process.

  - *count*  
    The number of elements to send from this process.

  - *datatype*  
    The data type of each element in the buffer. This parameter must be compatible with the operation as specified in the *op* parameter.

  - *op*  
    The global reduction operation to perform. The handle can indicate a built-in or application-defined operation. For a list of predefined operations, see the [**MPI\_Op**](mpi-op-enumeration.md) topic.

  - *root*  
    The rank of the receiving process within the specified communicator.

  - *comm*  
    The [**MPI\_Comm**](mpi-comm-enumeration.md) communicator handle.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_REDUCE(SENDBUF, RECVBUF, COUNT, DATATYPE, OP, ROOT, COMM, IERROR) 
        <type> SENDBUF(*), RECVBUF(*) 
        INTEGER COUNT, DATATYPE, OP, ROOT, COMM, IERROR
```

## Remarks

The **MPI\_Reduce** function is implemented with the assumption that the specified operation is associative. All predefined operations are designed to be associative and commutative. Users can define operations that are designed to be associative, but not commutative. The default evaluation order of a reduction operation is determined by the ranks of the processes in the group. However, the implementation can take advantage of associativity, or associativity and commutativity to change the order of evaluation. This process can change the result of the reduction for operations that are not strictly associative and commutative, such as floating point addition.

Some applications cannot ignore the non-associative nature of floating-point operations or might use user-defined operations that require a special order of evaluation and cannot be treated as associative. In this case, you can enforce the order of evaluation explicitly. For example, in the case of operations that require a strict left-to-right, or right-to-left, evaluation order, you can use the following process:

1.  Gather all operands at a single process, for example, by using the [**MPI\_Gather**](mpi-gather-function.md) function.
2.  Apply the reduction operation in the required order, for example, by using the [**MPI\_Reduce\_local**](mpi-reduce-local-function.md) function.
3.  If required, broadcast or scatter the result to the other processes.

> [!NOTE]
> It is possible to supply different user-defined operations to the **MPI\_Reduce** function in each process. The function does not define which operations are used on which operands in this case. You cannot make any assumptions about how the **MPI\_Reduce** function is implemented. It is safest to specify the same operation in each process.

 

User-defined operators can operate on general, derived data types. In this case, each argument that the reduce operation is applied to is one element that is described by such a data type, which can contain several basic values.

Overlapping data types are permitted in send buffers, but not in receive buffers. Overlapping data types in receive buffers can give unpredictable results and are considered an error.

If the *comm* parameter references an intracommunicator, the **MPI\_Reduce** function combines the elements as specified in the input buffer of each process in the group, and by using the specified operation, returns the combined value in the output buffer of the root process.

The input buffer and the output buffer have the same number of elements of the same data type. Call the function in all group members by using the same values for the *count*, *datatype*, *op*, *root*, and *comm* parameters. This practice ensures that all processes provide input buffers and output buffers of the same length, with elements of the same type.

Each process can provide one element, or a sequence of elements, in which case the operation is executed per element on each entry of the sequence. For example, if the operation is **MPI\_MAX** and the send buffer contains two elements that are floating point numbers, then `recvbuf(1)` receives the global maximum of `(sendbuf(1))` and `recvbuf(2)` receives the global maximum of `(sendbuf(2))`.

If the *comm* parameter references an intercommunicator, then the call involves all processes in the intercommunicator, but with one group, group A, that defines the root process. All processes in the other group, group B, set the same value in *root* parameter, that is, the rank of the root process in group A. The root process sets the value **MPI\_ROOT** in the *root* parameter. All other processes in group A set the value **MPI\_PROC\_NULL** in the *root* parameter. Only send buffer parameters are significant in group B processes and only receive buffer parameters are significant in the root process.

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

[**MPI\_Datatype**](mpi-datatype-enumeration.md)

[**MPI\_Gather**](mpi-gather-function.md)

[**MPI\_Op**](mpi-op-enumeration.md)

[**MPI\_Bcast**](mpi-bcast-function.md)

