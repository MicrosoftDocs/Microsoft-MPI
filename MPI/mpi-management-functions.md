---
title: MPI Management Functions
TOCTitle: MPI Management Functions
ms:assetid: F88C4C06-3AD5-454D-9A5B-1A895E32377F
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473433(v=VS.85)
ms:contentKeyID: 59360969
ms.date: 03/28/2018
mtps_version: v=VS.85
---

# MPI Management Functions

## In this section

  - [**MPI\_Abort**](mpi-abort-function.md)  
    Terminates MPI execution environment.

  - [**MPI\_Add\_error\_class**](mpi-add-error-class-function.md)  
    Adds an MPI error class to the known classes.

  - [**MPI\_Add\_error\_code**](mpi-add-error-code-function.md)  
    Adds an MPI error code to an MPI error class.

  - [**MPI\_Add\_error\_string**](mpi-add-error-string-function.md)  
    Associates an error string with an MPI error code or class.

  - [**MPI\_Alloc\_mem**](mpi-alloc-mem-function.md)  
    Allocates memory for message passing and RMA.

  - [**MPI\_Comm\_call\_errhandler**](mpi-comm-call-errhandler-function.md)  
    Calls the error handler installed on a communicator.

  - [**MPI\_Comm\_create\_errhandler**](mpi-comm-create-errhandler-function.md)  
    Creates an error handler for a communicator.

  - [*MPI\_Comm\_errhandler\_fn*](mpi-comm-errhandler-fn-callback-function.md)  
    [*MPI\_Comm\_errhandler\_fn*](mpi-comm-errhandler-fn-callback-function.md) is a placeholder for the application-defined function name.

  - [**MPI\_Comm\_get\_errhandler**](mpi-comm-get-errhandler-function.md)  
    Gets the error handler attached to a communicator.

  - [**MPI\_Comm\_set\_errhandler**](mpi-comm-set-errhandler-function.md)  
    Sets the error handler for a communicator.

  - [**MPI\_Errhandler\_create**](mpi-errhandler-create-function.md)  
    This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Comm\_create\_errhandler**](mpi-comm-create-errhandler-function.md) function.

  - [**MPI\_Errhandler\_free**](mpi-errhandler-free-function.md)  
    Sets the error handler for a communicator.

  - [**MPI\_Errhandler\_get**](mpi-errhandler-get-function.md)  
    This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Comm\_get\_errhandler**](mpi-comm-get-errhandler-function.md) function.

  - [**MPI\_Errhandler\_set**](mpi-errhandler-set-function.md)  
    This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Comm\_set\_errhandler**](mpi-comm-set-errhandler-function.md) function.

  - [**MPI\_Error\_class**](mpi-error-class-function.md)  
    Converts an error code to an error class.

  - [**MPI\_Error\_string**](mpi-error-string-function.md)  
    Returns a string for a given error code.

  - [**MPI\_File\_call\_errhandler**](mpi-file-call-errhandler-function.md)  
    Calls the error handler installed on a file.

  - [**MPI\_File\_create\_errhandler**](mpi-file-create-errhandler-function.md)  
    Creates a file error handler.

  - [*MPI\_File\_errhandler\_fn*](mpi-file-errhandler-fn-callback-function.md)  
    [*MPI\_File\_errhandler\_fn*](mpi-file-errhandler-fn-callback-function.md) is a placeholder for the application-defined function name.

  - [**MPI\_File\_get\_errhandler**](mpi-file-get-errhandler-function.md)  
    Gets the error handler attached to a file.

  - [**MPI\_File\_set\_errhandler**](mpi-file-set-errhandler-function.md)  
    Sets the error handler for an MPI file.

  - [**MPI\_Finalize**](mpi-finalize-function.md)  
    Terminates the calling MPI process’s execution environment.

  - [**MPI\_Finalized**](mpi-finalized-function.md)  
    Indicates whether [**MPI\_Finalize**](mpi-finalize-function.md) has been called.

  - [**MPI\_Free\_mem**](mpi-free-mem-function.md)  
    Frees the memory allocated with [**MPI\_Alloc\_mem**](mpi-alloc-mem-function.md).

  - [**MPI\_Get\_processor\_name**](mpi-get-processor-name-function.md)  
    Gets the name of the processor.

  - [**MPI\_Get\_version**](mpi-get-version-function.md)  
    Returns the version number of MPI.

  - [**MPI\_Init**](mpi-init-function.md)  
    Initializes the calling MPI process’s execution environment for single threaded execution.

  - [**MPI\_Initialized**](mpi-initialized-function.md)  
    Indicates whether [**MPI\_Init**](mpi-init-function.md) has been called.

  - [**MPI\_Win\_call\_errhandler**](mpi-win-call-errhandler-function.md)  
    Calls the error handler installed on a window object.

  - [**MPI\_Win\_create\_errhandler**](mpi-win-create-errhandler-function.md)  
    Creates an error handler for use with MPI window objects.

  - [*MPI\_Win\_errhandler\_fn*](mpi-win-errhandler-fn-callback-function.md)  
    [*MPI\_Win\_errhandler\_fn*](mpi-win-errhandler-fn-callback-function.md) is a placeholder for the application-defined function name.

  - [**MPI\_Win\_get\_errhandler**](mpi-win-get-errhandler-function.md)  
    Gets the error handler associated with MPI window object.

  - [**MPI\_Win\_set\_errhandler**](mpi-win-set-errhandler-function.md)  
    Sets an error handler for use with MPI window objects.

  - [**MPI\_Wtick**](mpi-wtick-function.md)  
    Returns the resolution of [**MPI\_Wtime**](mpi-wtime-function.md).

  - [**MPI\_Wtime**](mpi-wtime-function.md)  
    Returns an elapsed time on the calling processor.

