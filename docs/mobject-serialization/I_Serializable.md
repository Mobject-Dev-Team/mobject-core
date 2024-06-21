# I_Serializable Interface

## Definition

|             |                            |
| ----------- | -------------------------- |
| Namespace   | mobject-serializer         |
| Library     | mobject-serializer         |
| Inheritance | \_\_SYSTEM.IQueryInterface |
| Implements  |                            |

## Remarks

The `I_Serializable` interface provides a standard way to serialize objects. The type of serializer is not known by the object, which allows for Json, XML or any other string based type to be used.

## Methods

### SerializeWith(Serializer)

Serializes the object using the provided serializer.

#### Parameters

| Parameters | Datatype     | Description                                       |
| ---------- | ------------ | ------------------------------------------------- |
| Serializer | I_Serializer | The serializer to use for serializing the object. |

#### Return

N/A

## Properties

N/A

## Example Usage

To implement the `I_Serializable` interface, an object must define how it serializes itself. This typically involves specifying how each property of the object should be handled by the `Serializer` provided as an argument to the `SerializeWith` method.

```declaration
//IMPLEMENTATION OF I_Serializable
METHOD SerializeWith
VAR_INPUT
    Serializer : I_Serializer;
END_VAR
```

```body
// Detailed implementation to serialize the object's properties.
Serializer.StartObject();
Serializer.AddKeyString('Name', 'Example Object');
Serializer.AddKeyDint('ID', 12345);
Serializer.EndObject();
```

This interface ensures that all serializable objects within a project adhere to a consistent serialization mechanism, facilitating data exchange and persistence.
