# I_Error Interface

## Definition

|             |                |
| ----------- | -------------- |
| Namespace   | mobject-errors |
| Library     | mobject-errors |
| Inheritance | Disposable     |
| Implements  | I_Error        |

## Remarks

The Error abstract base class should be used to implement custom error classes. This provides inbuilt seralization functionality, and error comparison.

## Example

```declaration
FUNCTION_BLOCK MyError EXTENDS Error
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

### SerializeWith(Serializer)

Serializes the error using the provided serializer. To add more information to the serialization, you can override the OnSerialize(serializer) protected method. This will be called after the initial serialization data has been added.

#### Parameters

| Parameters | Datatype     | Description                                       |
| ---------- | ------------ | ------------------------------------------------- |
| Serializer | I_Serializer | The serializer to use for serializing the object. |

#### Return

N/A

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
