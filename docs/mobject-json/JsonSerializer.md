# JsonSerializer Class

## Definition

|             |                                                        |
| ----------- | ------------------------------------------------------ |
| Namespace   | mobject-json                                           |
| Library     | mobject-json                                           |
| Inheritance | [Disposable](./mobject-disposable/Disposable.md)       |
| Implements  | [I_Serializer](./mobject-serializable/I_Serializer.md) |

## Remarks

The JsonSerializer class serves as a critical component in our serialization architecture, designed to convert complex objects into a JSON format. It offers a suite of methods tailored for constructing JSON from various data types.

## Example

```declaration
PROGRAM Main
VAR
   jsonSerializer : JsonSerializer;
   out : STRING;
END_VAR
```

```body
// the serializer can be used using standard methods, or in the fluent style.
jsonSerializer.StartObject()
   .AddKeyDint('dint',123)
   .AddKeyBool('bool',TRUE)
   .AddKeyString('string','foobar')
   .AddKeyNull('null')
   .EndObject();

jsonSerializer.TryGetSerialziedData(ADR(out),SIZEOF(out));
// out = {"dint":123,"bool":true,"string":"foobar","null":null}
```

## Methods

### AddBase64(pBytes, nBytes) : I_Serializer

Adds an array of bytes to the document as a base64 encoded string.

#### Parameters

| Parameters | Datatype        | Description                                |
| ---------- | --------------- | ------------------------------------------ |
| pBytes     | POINTER TO BYTE | The pointer to the first byte of the array |
| nBytes     | DINT            | The number of bytes to use                 |

#### Return

| Datatype                                               | Description                                                                   |
| ------------------------------------------------------ | ----------------------------------------------------------------------------- |
| [I_Serializer](./mobject-serializable/I_Serializer.md) | The same instance of the serializer, enabling chained or fluent method calls. |

#### Usage

```example
// Initialize variables
rawData : ARRAY[0..4] OF BYTE := [104, 101, 108, 108, 111]; // The bytes to be added
out : STRING; // String to hold the serialized output
result : BOOL; // Boolean indicating the success of the operation

// Add the array as base64 and attempt to retrieve the serialized data
jsonSerializer.AddBase64(ADR(rawData), SIZEOF(rawData));  // Adds the array to the document
result := jsonSerializer.TryGetSerializedData(ADR(out), SIZEOF(out));  // Retrieves the serialized data

// The expected outcome
// result = true, indicating success
// out = '"aGVsbG8="', representing the serialized data
```

### AddBool(Value) : I_Serializer

Adds a boolean value to the document, allowing for fluent coding with subsequent method calls.

#### Parameters

| Parameters | Datatype | Description                                                                   |
| ---------- | -------- | ----------------------------------------------------------------------------- |
| Value      | BOOL     | The boolean value (TRUE or FALSE) that needs to be encoded into the document. |

#### Return

| Datatype                                               | Description                                                                    |
| ------------------------------------------------------ | ------------------------------------------------------------------------------ |
| [I_Serializer](./mobject-serializable/I_Serializer.md) | The same instance of the serializer, enabling chained or fluent method calls.g |

#### Usage

```example
// Initialize variables
value : BOOL := TRUE;  // The boolean to be added
out : STRING;          // String to hold the serialized output
result : BOOL;         // Boolean indicating the success of the operation

// Add the boolean value and attempt to retrieve the serialized data
jsonSerializer.AddBool(value);  // Adds the boolean to the document
result := jsonSerializer.TryGetSerializedData(ADR(out), SIZEOF(out));  // Retrieves the serialized data

// The expected outcome
// result = true, indicating success
// out = 'true', representing the serialized boolean
```

### AddByte(Value) : I_Serializer

Documentation coming soon...

### AddBytesAsHex(pBytes, nBytes) : I_Serializer

Documentation coming soon...

### AddDateTime(Value) : I_Serializer

Documentation coming soon...

### AddDcTime(Value) : I_Serializer

Documentation coming soon...

### AddDint(Value) : I_Serializer

Documentation coming soon...

### AddDword(Value) : I_Serializer

Documentation coming soon...

### AddFileTime(Value) : I_Serializer

Documentation coming soon...

### AddInt(Value) : I_Serializer

Documentation coming soon...

### AddKey(Value) : I_Serializer

Documentation coming soon...

### AddKeyBase64(Key, pBytes, nBytes) : I_Serializer

Adds an array of bytes to the document as a base64 encoded string as a key value pair.

#### Parameters

| Parameters | Datatype        | Description                                |
| ---------- | --------------- | ------------------------------------------ |
| Key        | T_MAXSTRING     | The String representing the key            |
| pBytes     | POINTER TO BYTE | The pointer to the first byte of the array |
| nBytes     | DINT            | The number of bytes to use                 |

#### Return

| Datatype                                               | Description                                                                   |
| ------------------------------------------------------ | ----------------------------------------------------------------------------- |
| [I_Serializer](./mobject-serializable/I_Serializer.md) | The same instance of the serializer, enabling chained or fluent method calls. |

#### Usage

```example
// definition
rawData : ARRAY[0..4] OF BYTE := [104, 101, 108, 108, 111];
out : STRING;
result : BOOL;

// body
jsonSerializer.AddKeyBase64('data', ADR(rawData), SIZEOF(rawData));
result := jsonSerializer.TryGetSerialziedData(ADR(out),SIZEOF(out));
// result = true, out = '{"data":"aGVsbG8="}'
```

### AddKeyBool(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyByte(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyBytesAsHex(Key, pBytes, nBytes) : I_Serializer

Documentation coming soon...

### AddKeyDateTime(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyDcTime(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyDint(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyDword(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyFileTime(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyInt(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyLint(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyLreal(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyLtime(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyLword(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyNull(Key) : I_Serializer

Documentation coming soon...

### AddKeyRawObject(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyReal(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeySint(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyString(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyStringByRef(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyTime(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyTod(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyUdint(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyUint(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyUlint(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyUsint(Key, Value) : I_Serializer

Documentation coming soon...

### AddKeyWord(Key, Value) : I_Serializer

Documentation coming soon...

### AddLint(Value) : I_Serializer

Documentation coming soon...

### AddLreal(Value) : I_Serializer

Documentation coming soon...

### AddLtime(Value) : I_Serializer

Documentation coming soon...

### AddLword(Value) : I_Serializer

Documentation coming soon...

### AddNull() : I_Serializer

Documentation coming soon...

### AddRawObject(RawObject) : I_Serializer

Documentation coming soon...

### AddReal(Value) : I_Serializer

Documentation coming soon...

### AddSint(Value) : I_Serializer

Documentation coming soon...

### AddString(Value) : I_Serializer

Documentation coming soon...

### AddStringByRef(Value) : I_Serializer

Documentation coming soon...

### AddTime(Value) : I_Serializer

Documentation coming soon...

### AddTod(Value) : I_Serializer

Documentation coming soon...

### AddUdint(Value) : I_Serializer

Documentation coming soon...

### AddUint(Value) : I_Serializer

Documentation coming soon...

### AddUlint(Value) : I_Serializer

Documentation coming soon...

### AddUsint(Value) : I_Serializer

Documentation coming soon...

### AddWord(Value) : I_Serializer

Documentation coming soon...

### Clone() : I_Serializer

Documentation coming soon...

### EndArray() : I_Serializer

Documentation coming soon...

### EndObject() : I_Serializer

Documentation coming soon...

### EndArray() : I_Serializer

Documentation coming soon...

### GetSeralizedDataLength() : UDINT

Documentation coming soon...

### Reset()

Documentation coming soon...

### StartArray() : I_Serializer

Documentation coming soon...

### StartObject() : I_Serializer

Documentation coming soon...

### TryCopySerialziedData(DestinationAddress, DestinationSize) : BOOL

Documentation coming soon...

### TryGetSerialziedData(DestinationAddress, DestinationSize) : BOOL

Documentation coming soon...
