# I_Serializer Interface

## Definition

|             |                                                      |
| ----------- | ---------------------------------------------------- |
| Namespace   | mobject-seralizer                                    |
| Library     | mobject-seralizer                                    |
| Inheritance | [I_Disposable](./mobject-disposable/I_Disposable.md) |
| Implements  |                                                      |

## Remarks

The `I_Serializer` interface is designed to facilitate the serialization of various data types in a structured manner. It extends the [I_Disposable](./mobject-disposable/I_Disposable.md) interface, indicating that instances of `I_Serializer` should be disposed of properly to release resources. The interface provides a wide range of methods to add data of different types to the serialization stream, including primitive types, arrays, and complex objects implementing the `I_Serializable` interface. Additionally, it offers functionality to manage the serialization state, such as starting and ending objects and arrays, and methods to retrieve or reset the serialized data.

## Methods

### Basic Data Type Methods

These methods allow adding basic data types to the serialization stream. Each method specifies the data type it adds, such as `BOOL`, `BYTE`, `DINT`, etc., and accepts the data value as an input parameter.

- **AddBase64(pBytes, nBytes)**: Adds a base64 encoded string representation of the byte array.
- **AddBool(Value)**: Adds a boolean value.
- **AddByte(Value)**: Adds a byte value.
- **AddBytesAsHex(pBytes, nBytes)**: Adds a hexadecimal string representation of the byte array.
- **AddDateTime(Value)**: Adds a `DATE_AND_TIME` value.
- **AddDcTime(Value)**: Adds a `DCTIME` value.
- **AddDint(Value)**: Adds a double integer (DINT) value.
- **AddDword(Value)**: Adds a double word (DWORD) value.
- ... (Other primitive data types follow a similar pattern.)

### Key-Value Pair Methods

These methods allow adding key-value pairs, where the key is a string, and the value is one of the supported data types. These methods are crucial for creating structured data like JSON objects.

- **AddKey(Key, Value)**: Adds a key with a specific value, where the value's data type is determined by the method variant (e.g., `AddKeyBool`, `AddKeyInt`, etc.).
- **AddKeyBase64(Key, pBytes, nBytes)**: Adds a base64 encoded string for a byte array under a specified key.
- **AddKeyBool(Key, Value)**: Adds a boolean value under a specified key.
- **AddKeyByte(Key, Value)**: Adds a byte value under a specified key.
- ... (Other key-value methods follow a similar pattern for different data types.)

### Array and Object Management Methods

- **StartArray()**: Indicates the start of an array in the serialization stream.
- **EndArray()**: Indicates the end of an array in the serialization stream.
- **StartObject()**: Indicates the start of an object in the serialization stream.
- **EndObject()**: Indicates the end of an object in the serialization stream.

### Serialization Control Methods

- **Clone()**: Creates a new instance of the serializer that is a clone of the current instance.
- **Reset()**: Resets the serializer, clearing the current serialization state and data.
- **GetSerializedDataLength()**: Returns the length of the serialized data.
- **TryCopySerializedData(DestinationAddress, DestinationSize)**: Attempts to copy the serialized data to a specified destination.
- **TryGetSerializedData(DestinationAddress, DestinationSize)**: Attempts to get the serialized data, providing a boolean result indicating success.

## Example Usage

The following example demonstrates how to use the `I_Serializer` interface to serialize a simple object:

```plaintext
VAR
	mySerializer: I_Serializer;
	myString : T_MAXSTRING;
	result : BOOL;
END_VAR

mySerializer.StartObject();
mySerializer.AddKeyString('Name', 'Example Object');
mySerializer.AddKeyDint('ID', 12345);
mySerializer.EndObject();
result := mySerializer.TryGetSerializedData(ADR(myString), SIZEOF(myString)); // result = TRUE, myString = '{"Name":"Example Object","ID":12345}'
```
