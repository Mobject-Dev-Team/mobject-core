# I_Deserializable Interface

## Definition

|             |                            |
| ----------- | -------------------------- |
| Namespace   | mobject-serialization      |
| Library     | mobject-serialization      |
| Inheritance | \_\_SYSTEM.IQueryInterface |
| Implements  |                            |

## Remarks

The `I_Deserializable` interface is designed to provide a standardized approach for deserializing objects. It ensures that objects can be restored from a serialized state, enabling efficient data exchange and state management across different components of a PLC application.

## Methods

### TryDeserializeFrom(Deserializer, Feedback) : BOOL

Attempts to deserialize an object from the provided deserializer.

#### Parameters

| Parameters   | Datatype               | Description                                                            |
| ------------ | ---------------------- | ---------------------------------------------------------------------- |
| Deserializer | I_Deserializer         | The deserializer to use for attempting to deserialize the object.      |
| Feedback     | I_DeserializerFeedback | The a feedback object which can be used to hold deserialization errors |

#### Returns

| Return Value | Datatype | Description                                       |
| ------------ | -------- | ------------------------------------------------- |
| Result       | BOOL     | Indicates whether deserialization was successful. |

## Example Usage

To implement the `I_Deserializable` interface, an object must define how it deserializes itself. This typically involves specifying how each property of the object should be written to by the `Deserializer` provided as an argument to the `TryDeserializeFrom` method.

```declaration
//IMPLEMENTATION OF I_Deserializable
METHOD TryDeserializeFrom
VAR_INPUT
    Deserializer : I_Deserializer;
	Feedback : I_DeserialzerFeedback;
END_VAR
```

```body
// Detailed implementation to deserialize the object's state.
// This example is from _TIMESTRUCT
TryDeserializeFrom :=
	Deserializer.TryGetKeyWord('wYear',data.wYear, Feedback) AND
	Deserializer.TryGetKeyWord('wMonth',data.wMonth, Feedback) AND
	Deserializer.TryGetKeyWord('wDayOfWeek',data.wDayOfWeek, Feedback) AND
	Deserializer.TryGetKeyWord('wDay',data.wDay, Feedback) AND
	Deserializer.TryGetKeyWord('wHour',data.wHour, Feedback) AND
	Deserializer.TryGetKeyWord('wMinute',data.wMinute, Feedback) AND
	Deserializer.TryGetKeyWord('wSecond',data.wSecond, Feedback) AND
	Deserializer.TryGetKeyWord('wMilliseconds',data.wMilliseconds, Feedback);
```
