---
description: Reserved Parameters
ms.custom: PSSA v1.21.0
ms.date: 06/28/2023
ms.topic: reference
title: ReservedParams
---
# ReservedParams

**Severity Level: Error**

## Description

You cannot use reserved common parameters in an advanced function.

## How

Change the name of the parameter.

## Example

### Wrong

```powershell
function Test
{
    [CmdletBinding]
    Param
    (
        $ErrorVariable,
        $Parameter2
    )
}
```

### Correct

```powershell
function Test
{
    [CmdletBinding]
    Param
    (
        $Err,
        $Parameter2
    )
}
```
