---
title: MPI_Datatype enumeration
TOCTitle: MPI_Datatype enumeration
ms:assetid: FA174D3F-F696-4A0F-89C7-2193A88EF799
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473290(v=VS.85)
ms:contentKeyID: 59360836
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_2COMPLEX
- mpi/MPI_2DOUBLE_COMPLEX
- mpi/MPI_2DOUBLE_PRECISION
- mpi/MPI_2INT
- mpi/MPI_2INTEGER
- mpi/MPI_2REAL
- mpi/MPI_AINT
- mpi/MPI_BYTE
- mpi/MPI_C_BOOL
- mpi/MPI_C_COMPLEX
- mpi/MPI_C_DOUBLE_COMPLEX
- mpi/MPI_C_FLOAT_COMPLEX
- mpi/MPI_C_LONG_DOUBLE_COMPLEX
- mpi/MPI_CHAR
- mpi/MPI_CHARACTER
- mpi/MPI_COMPLEX
- mpi/MPI_COMPLEX16
- mpi/MPI_COMPLEX32
- mpi/MPI_COMPLEX4
- mpi/MPI_COMPLEX8
- mpi/MPI_Datatype
- mpi/MPI_DATATYPE_NULL
- mpi/MPI_DOUBLE
- mpi/MPI_DOUBLE_COMPLEX
- mpi/MPI_DOUBLE_INT
- mpi/MPI_DOUBLE_PRECISION
- mpi/MPI_FLOAT
- mpi/MPI_FLOAT_INT
- mpi/MPI_INT
- MPI_C_BOOL
- mpi/MPI_WCHAR
- mpi/MPI_INT64_T
- mpi/MPI_REAL2
- mpi/MPI_INTEGER1
- mpi/MPI_REAL4
- MPI_COMPLEX8
- MPI_C_FLOAT_COMPLEX
- mpi/MPI_INTEGER16
- mpi/MPI_LB
- mpi/MPI_UINT8_T
- MPI_2COMPLEX
- mpi/MPI_LONG_LONG
- mpi/MPI_UNSIGNED
- MPI_C_DOUBLE_COMPLEX
- MPI_COMPLEX
- MPI_C_LONG_DOUBLE_COMPLEX
- mpi/MPI_UINT32_T
- mpi/MPI_UINT64_T
- MPI_COMPLEX16
- mpi/MPI_UNSIGNED_CHAR
- mpi/MPI_INT32_T
- mpi/MPI_LONG_INT
- mpi/MPI_INT16_T
- mpi/MPI_UB
- mpi/MPI_REAL8
- mpi/MPI_INTEGER8
- mpi/MPI_REAL16
- mpi/MPI_UINT16_T
- mpi/MPI_LONG_DOUBLE_INT
- mpi/MPI_INTEGER2
- MPI_2INTEGER
- mpi/MPI_LONG_DOUBLE
- mpi/MPI_SHORT
- mpi/MPI_SHORT_INT
- mpi/MPI_OFFSET
- MPI_AINT
- mpi/MPI_SIGNED_CHAR
- MPI_2INT
- MPI_COMPLEX4
- MPI_CHAR
- MPI_CHARACTER
- mpi/MPI_REAL
- MPI_2REAL
- mpi/MPI_UNSIGNED_SHORT
- mpi/MPI_INTEGER
- mpi/MPI_UNSIGNED_LONG_LONG
- MPI_Datatype
- MPI_BYTE
- mpi/MPI_LOGICAL
- MPI_2DOUBLE_COMPLEX
- MPI_C_COMPLEX
- MPI_2DOUBLE_PRECISION
- mpi/MPI_LONG
- mpi/MPI_UNSIGNED_LONG
- mpi/MPI_INT8_T
- mpi/MPI_INTEGER4
- mpi/MPI_PACKED
- MPI_COMPLEX32
- mpi/MPI_LONG_LONG_INT
- MPI_SHORT_INT
- MPI_LONG_LONG
- MPI_UNSIGNED
- MPI_FLOAT_INT
- MPI_REAL2
- MPI_INTEGER2
- MPI_LB
- MPI_INT16_T
- MPI_INTEGER
- MPI_INT8_T
- MPI_INTEGER1
- MPI_UNSIGNED_LONG
- MPI_INT
- MPI_WCHAR
- MPI_UINT16_T
- MPI_LONG_INT
- MPI_UNSIGNED_SHORT
- MPI_UINT8_T
- MPI_OFFSET
- MPI_DOUBLE_PRECISION
- MPI_SHORT
- MPI_INTEGER4
- MPI_SIGNED_CHAR
- MPI_REAL8
- MPI_LONG_LONG_INT
- MPI_UINT64_T
- MPI_FLOAT
- MPI_LONG_DOUBLE_INT
- MPI_UB
- MPI_DOUBLE
- MPI_INTEGER8
- MPI_INT32_T
- MPI_DATATYPE_NULL
- MPI_LONG
- MPI_LOGICAL
- MPI_INT64_T
- MPI_REAL4
- MPI_UNSIGNED_CHAR
- MPI_PACKED
- MPI_UNSIGNED_LONG_LONG
- MPI_UINT32_T
- MPI_LONG_DOUBLE
- MPI_INTEGER16
- MPI_REAL
- MPI_DOUBLE_COMPLEX
- MPI_DOUBLE_INT
- MPI_REAL16
dev_langs:
- C++
- C
api_location:
- mpi.h
api_name:
- MPI_Datatype
api_type:
- HeaderDef
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Explore the enumeration of predefined MPI datatypes at Microsoft's learning platform. Understand syntax, constants, and requirements.
---

# MPI\_Datatype enumeration

The enumeration of predefined MPI datatypes.

## Syntax

``` c++
typedef enum _MPI_Datatype { 
  MPI_DATATYPE_NULL          = 0x0c000000,
  MPI_CHAR                   = 0x4c000101,
  MPI_UNSIGNED_CHAR          = 0x4c000102,
  MPI_SHORT                  = 0x4c000203,
  MPI_UNSIGNED_SHORT         = 0x4c000204,
  MPI_INT                    = 0x4c000405,
  MPI_UNSIGNED               = 0x4c000406,
  MPI_LONG                   = 0x4c000407,
  MPI_UNSIGNED_LONG          = 0x4c000408,
  MPI_LONG_LONG_INT          = 0x4c000809,
  MPI_LONG_LONG              = MPI_LONG_LONG_INT,
  MPI_FLOAT                  = 0x4c00040a,
  MPI_DOUBLE                 = 0x4c00080b,
  MPI_LONG_DOUBLE            = 0x4c00080c,
  MPI_BYTE                   = 0x4c00010d,
  MPI_WCHAR                  = 0x4c00020e,
  MPI_PACKED                 = 0x4c00010f,
  MPI_LB                     = 0x4c000010,
  MPI_UB                     = 0x4c000011,
  MPI_C_COMPLEX              = 0x4c000812,
  MPI_C_FLOAT_COMPLEX        = 0x4c000813,
  MPI_C_DOUBLE_COMPLEX       = 0x4c001614,
  MPI_C_LONG_DOUBLE_COMPLEX  = 0x4c001615,
  MPI_2INT                   = 0x4c000816,
  MPI_C_BOOL                 = 0x4c000117,
  MPI_SIGNED_CHAR            = 0x4c000118,
  MPI_UNSIGNED_LONG_LONG     = 0x4c000819,
  MPI_CHARACTER              = 0x4c00011a,
  MPI_INTEGER                = 0x4c00041b,
  MPI_REAL                   = 0x4c00041c,
  MPI_LOGICAL                = 0x4c00041d,
  MPI_COMPLEX                = 0x4c00081e,
  MPI_DOUBLE_PRECISION       = 0x4c00081f,
  MPI_2INTEGER               = 0x4c000820,
  MPI_2REAL                  = 0x4c000821,
  MPI_DOUBLE_COMPLEX         = 0x4c001022,
  MPI_2DOUBLE_PRECISION      = 0x4c001023,
  MPI_2COMPLEX               = 0x4c001024,
  MPI_2DOUBLE_COMPLEX        = 0x4c002025,
  MPI_REAL2                  = MPI_DATATYPE_NULL,
  MPI_REAL4                  = 0x4c000427,
  MPI_COMPLEX8               = 0x4c000828,
  MPI_REAL8                  = 0x4c000829,
  MPI_COMPLEX16              = 0x4c00102a,
  MPI_REAL16                 = MPI_DATATYPE_NULL,
  MPI_COMPLEX32              = MPI_DATATYPE_NULL,
  MPI_INTEGER1               = 0x4c00012d,
  MPI_COMPLEX4               = MPI_DATATYPE_NULL,
  MPI_INTEGER2               = 0x4c00022f,
  MPI_INTEGER4               = 0x4c000430,
  MPI_INTEGER8               = 0x4c000831,
  MPI_INTEGER16              = MPI_DATATYPE_NULL,
  MPI_INT8_T                 = 0x4c000133,
  MPI_INT16_T                = 0x4c000234,
  MPI_INT32_T                = 0x4c000435,
  MPI_INT64_T                = 0x4c000836,
  MPI_UINT8_T                = 0x4c000137,
  MPI_UINT16_T               = 0x4c000238,
  MPI_UINT32_T               = 0x4c000439,
  MPI_UINT64_T               = 0x4c00083a,
  MPI_AINT                   = 0x4c00083b (_WIN64), 0x4c00043b,
  MPI_OFFSET                 = 0x4c00083c,
  MPI_FLOAT_INT              = 0x8c000000,
  MPI_DOUBLE_INT             = 0x8c000001,
  MPI_LONG_INT               = 0x8c000002,
  MPI_SHORT_INT              = 0x8c000003,
  MPI_LONG_DOUBLE_INT        = 0x8c000004
} MPI_Datatype;
```

## Constants

  - **MPI\_DATATYPE\_NULL**

  - **MPI\_CHAR**

  - **MPI\_UNSIGNED\_CHAR**

  - **MPI\_SHORT**

  - **MPI\_UNSIGNED\_SHORT**

  - **MPI\_INT**

  - **MPI\_UNSIGNED**

  - **MPI\_LONG**

  - **MPI\_UNSIGNED\_LONG**

  - **MPI\_LONG\_LONG\_INT**

  - **MPI\_LONG\_LONG**

  - **MPI\_FLOAT**

  - **MPI\_DOUBLE**

  - **MPI\_LONG\_DOUBLE**

  - **MPI\_BYTE**

  - **MPI\_WCHAR**

  - **MPI\_PACKED**

  - **MPI\_LB**

  - **MPI\_UB**

  - **MPI\_C\_COMPLEX**

  - **MPI\_C\_FLOAT\_COMPLEX**

  - **MPI\_C\_DOUBLE\_COMPLEX**

  - **MPI\_C\_LONG\_DOUBLE\_COMPLEX**

  - **MPI\_2INT**

  - **MPI\_C\_BOOL**

  - **MPI\_SIGNED\_CHAR**

  - **MPI\_UNSIGNED\_LONG\_LONG**

  - **MPI\_CHARACTER**

  - **MPI\_INTEGER**

  - **MPI\_REAL**

  - **MPI\_LOGICAL**

  - **MPI\_COMPLEX**

  - **MPI\_DOUBLE\_PRECISION**

  - **MPI\_2INTEGER**

  - **MPI\_2REAL**

  - **MPI\_DOUBLE\_COMPLEX**

  - **MPI\_2DOUBLE\_PRECISION**

  - **MPI\_2COMPLEX**

  - **MPI\_2DOUBLE\_COMPLEX**

  - **MPI\_REAL2**

  - **MPI\_REAL4**

  - **MPI\_COMPLEX8**

  - **MPI\_REAL8**

  - **MPI\_COMPLEX16**

  - **MPI\_REAL16**

  - **MPI\_COMPLEX32**

  - **MPI\_INTEGER1**

  - **MPI\_COMPLEX4**

  - **MPI\_INTEGER2**

  - **MPI\_INTEGER4**

  - **MPI\_INTEGER8**

  - **MPI\_INTEGER16**

  - **MPI\_INT8\_T**

  - **MPI\_INT16\_T**

  - **MPI\_INT32\_T**

  - **MPI\_INT64\_T**

  - **MPI\_UINT8\_T**

  - **MPI\_UINT16\_T**

  - **MPI\_UINT32\_T**

  - **MPI\_UINT64\_T**

  - **MPI\_AINT**

  - **MPI\_OFFSET**

  - **MPI\_FLOAT\_INT**

  - **MPI\_DOUBLE\_INT**

  - **MPI\_LONG\_INT**

  - **MPI\_SHORT\_INT**

  - **MPI\_LONG\_DOUBLE\_INT**

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
<td>Mpi.h</td>
</tr>
</tbody>
</table>


## See also

[MPI Enumerations](mpi-enumerations.md)

