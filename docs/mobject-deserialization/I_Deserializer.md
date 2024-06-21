# I_Deserializer Interface

## Definition

|             |                       |
| ----------- | --------------------- |
| Namespace   | mobject-serialization |
| Library     | mobject-serialization |
| Inheritance | I_Disposable          |

## Remarks

The `I_Deserializer` interface extends `I_Disposable` to provide methods for deserialization. It includes functionality to deserialize arrays, elements by index, and various data types from a serialized format.

## Methods

### GetArray() : I_Deserializer

Returns a deserializer for an array.

### GetElementByIndex(Index: UDINT) : I_Deserializer

Returns a deserializer for an array element using its index.

#### Parameters

| Parameters | Datatype | Description               |
| ---------- | -------- | ------------------------- |
| Index      | UDINT    | The index of the element. |

### GetKey(Key: T_MAXSTRING) : I_Deserializer

Returns a deserializer for a key.

#### Parameters

| Parameters | Datatype    | Description           |
| ---------- | ----------- | --------------------- |
| Key        | T_MAXSTRING | The key of the value. |

### GetKeyArray(Key: T_MAXSTRING) : I_Deserializer

Returns a deserializer for an array located by its key.

#### Parameters

| Parameters | Datatype    | Description           |
| ---------- | ----------- | --------------------- |
| Key        | T_MAXSTRING | The key of the array. |

### TryDeserializeKeyToObject(Key: T_MAXSTRING, Object: I_Deserializable, Feedback : I_DeserializerFeedback) : BOOL

Attempts to deserialize a key to an object.

#### Parameters

| Parameters | Datatype               | Description                                                            |
| ---------- | ---------------------- | ---------------------------------------------------------------------- |
| Key        | T_MAXSTRING            | The key of the object to deserialize.                                  |
| Object     | I_Deserializable       | The object to deserialize to.                                          |
| Feedback   | I_DeserializerFeedback | The a feedback object which can be used to hold deserialization errors |

#### Returns

| Return Value | Datatype | Description                                     |
| ------------ | -------- | ----------------------------------------------- |
| Result       | BOOL     | Indicates whether the operation was successful. |

### TryDeserializeToObject(Object: I_Deserializable, Feedback : I_DeserializerFeedback) : BOOL

Attempts to deserialize data to an object.

#### Parameters

| Parameters | Datatype               | Description                                                            |
| ---------- | ---------------------- | ---------------------------------------------------------------------- |
| Object     | I_Deserializable       | The object to deserialize to.                                          |
| Feedback   | I_DeserializerFeedback | The a feedback object which can be used to hold deserialization errors |

#### Returns

| Return Value | Datatype | Description                                     |
| ------------ | -------- | ----------------------------------------------- |
| Result       | BOOL     | Indicates whether the operation was successful. |

### TryGetBase64(pBytes: POINTER TO BYTE, nBytes: DINT, Feedback : I_DeserializerFeedback) : BOOL

Attempts to deserialize a Base64 encoded string into bytes.

#### Parameters

| Parameters | Datatype               | Description                                                            |
| ---------- | ---------------------- | ---------------------------------------------------------------------- |
| pBytes     | POINTER TO BYTE        | Pointer to the byte array to fill.                                     |
| nBytes     | DINT                   | The number of bytes to deserialize.                                    |
| Feedback   | I_DeserializerFeedback | The a feedback object which can be used to hold deserialization errors |

#### Returns

| Return Value | Datatype | Description                                     |
| ------------ | -------- | ----------------------------------------------- |
| Result       | BOOL     | Indicates whether the operation was successful. |

### TryGetBool(Destination: REFERENCE TO BOOL, Feedback : I_DeserializerFeedback) : BOOL

Attempts to deserialize a boolean value.

#### Parameters

| Parameters  | Datatype               | Description                                                            |
| ----------- | ---------------------- | ---------------------------------------------------------------------- |
| Destination | REFERENCE TO BOOL      | The reference to store the value.                                      |
| Feedback    | I_DeserializerFeedback | The a feedback object which can be used to hold deserialization errors |

#### Returns

| Return Value | Datatype | Description                                     |
| ------------ | -------- | ----------------------------------------------- |
| Result       | BOOL     | Indicates whether the operation was successful. |

... (Similar structure for other TryGet and TryGetKey methods, each tailored to their specific data type and parameters.)
