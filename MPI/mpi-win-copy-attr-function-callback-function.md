---
title: MPI_Win_copy_attr_function callback function
TOCTitle: MPI_Win_copy_attr_function callback function
ms:assetid: 4866238c-2fd2-43ee-938f-c36ca0ca0806
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520595(v=VS.85)
ms:contentKeyID: 59361066
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_Win_copy_attr_function
- mpi/WIN_COPY_ATTR_FUNCTION
- MPI_Win_copy_attr_function
- mpif/MPI_Win_copy_attr_function
- mpif/WIN_COPY_ATTR_FUNCTION
- WIN_COPY_ATTR_FUNCTION
dev_langs:
- C++
- C
---

# MPI\_Win\_copy\_attr\_function callback function

**MPI\_Win\_copy\_attr\_function** is a placeholder for the application-defined function name. It is a copy callback function for win_keyval.

## Syntax

``` c++
int MPI_Win_copy_attr_function(
           MPI_Win oldwin,
           int     win_keyval,
  _In_opt_ void    *extra_state,
  _In_     void    *attribute_val_in,
  _Out_    void    *attribute_val_out,
  _Out_    int     *flag
);
```

## Parameters

  - *oldwin*  
    Old MPI window.

  - *win\_keyval*  
    Window key value.

  - *extra\_state* \[in, optional\]  
    Extra state.

  - *attribute\_val\_in* \[in\]  
    Input value of the attribute.

  - *attribute\_val\_out* \[out\]  
    Output value of the attribute.

  - *flag* \[out\]  
    Flag value indicating if the copy was successful.

## Return value

If an attribute copy function returns anything other than **MPI\_SUCCESS**, then the call that caused it to be invoked is erroneous.

## Fortran

``` FORTRAN
    SUBROUTINE WIN_COPY_ATTR_FUNCTION(OLDWIN, WIN_KEYVAL, EXTRA_STATE,
                ATTRIBUTE_VAL_IN, ATTRIBUTE_VAL_OUT, FLAG, IERROR)
        INTEGER OLDWIN, WIN_KEYVAL, IERROR
        INTEGER(KIND=MPI_ADDRESS_KIND) EXTRA_STATE, ATTRIBUTE_VAL_IN,
            ATTRIBUTE_VAL_OUT
        LOGICAL FLAG
```

## Requirements

<table>
<colgroup>
<col/>
<col/>
</colgroup>
<tbody>
<tr class="odd">
<td><p>Header</p></td>
<td>Mpi.h;
Mpif.h</td>
</tr>
</tbody>
</table>


## See also

[MPI Caching Functions](mpi-caching-functions.md)

[**MPI\_Win\_create\_keyval**](mpi-win-create-keyval-function.md)

