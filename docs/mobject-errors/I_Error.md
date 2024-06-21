# I_Error Interface

## Definition

|             |                                                            |
| ----------- | ---------------------------------------------------------- |
| Namespace   | mobject-errors                                             |
| Library     | mobject-errors                                             |
| Inheritance | [I_Serializable](./mobject-serializable/I_Serializable.md) |
| Implements  |                                                            |

## Remarks

The I_Error interface should be implemented by any error class.

## Example

```declaration
FUNCTION_BLOCK MyError IMPLEMENTS I_Error
VAR
END_VAR
```

```body
//... no code should go here.
```

## Methods

### Accept(Visitor)

Visitor pattern implementation. Allows for error visitors.

#### Parameters

| Parameters | Datatype       | Description |
| ---------- | -------------- | ----------- |
| Visitor    | I_ErrorVisitor | The visitor |

#### Return

N/A

### IsSameAs(Error)

Checks to see if the current error is the same type as the supplied error.

#### Parameters

| Parameters | Datatype | Description                   |
| ---------- | -------- | ----------------------------- |
| Error      | I_Error  | The error to compare against. |

#### Return

| Datatype | Description                  |
| -------- | ---------------------------- |
| BOOL     | The error types are the same |

## Properties

### ErrorType

Returns the type of the error. This is used instead of an error code. When comparing errors with .IsSameAs() the error types will be compared.

#### Return

| Datatype    | Description |
| ----------- | ----------- |
| T_MAXSTRING | Error Type  |

### Message

Returns the message of the error

#### Return

| Datatype    | Description   |
| ----------- | ------------- |
| T_MAXSTRING | Error Message |
