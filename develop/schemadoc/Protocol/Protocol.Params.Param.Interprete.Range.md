---
uid: Protocol.Params.Param.Interprete.Range
---

# Range element

Defines a range for the parameter values.

## Parent

[Interprete](xref:Protocol.Params.Param.Interprete)

## Children

|Name|Occurrences|Description|
|--- |--- |--- |
|***Sequence***|||
|&nbsp;&nbsp;[Low](xref:Protocol.Params.Param.Interprete.Range.Low)|[0, 1]|Specifies the lower limit of the range, i.e. the minimum value of a parameter.|
|&nbsp;&nbsp;[High](xref:Protocol.Params.Param.Interprete.Range.High)|[0, 1]|Specifies the upper limit of the range, i.e. the maximum value of a parameter.|

## Remarks

By adding a range to the Protocol.Params.Param.Interprete tag, a value outside this defined range will be ignored. The limits of the range are defined by the Protocol.Params.Param.Interprete.Range.Low and Protocol.Params.Param.Interprete.Range.High tags.

> [!NOTE]
>
> - It's recommended to only use the Range tag for communication parameters (i.e. SNMP parameter).
    When a successful response was received, but the value is out of the interprete specified range, the value will not be set to the parameter (leaving it on it's previous value or not-intialized).
> - The Range tag can also be used to specify a value range in case of a simulated element.
> - From a QAction, it is possible to set a value that is outside of this range.
