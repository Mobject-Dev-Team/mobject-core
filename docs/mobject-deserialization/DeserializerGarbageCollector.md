# DeserializerGarbageCollector Function Block

## Overview

The `DeserializerGarbageCollector` function block is designed to manage the lifecycle of deserializers in a TwinCAT PLC project. It extends the `Disposable` class and implements the `I_DeserializerGarbageCollector` interface, offering functionality to register, deregister, and dispose of deserializer instances.

## Namespace

|             |                                |
| ----------- | ------------------------------ |
| Namespace   | mobject-serialization          |
| Library     | mobject-serialization          |
| Inheritance | Disposable                     |
| Implements  | I_DeserializerGarbageCollector |

## Remarks

This class is a helper class. It can be used to manage the lifecycle of deserializer child nodes. See mobject-json JsonDeserializer for an example of its use.

## Attributes

- `linkalways`
- `no_explicit_call` := 'This FB is a CLASS and must be accessed using methods or properties'
- `enable_dynamic_creation`

## Variables

| Variables     | Type  | Description                      |
| ------------- | ----- | -------------------------------- |
| deserializers | Stack | A stack to manage deserializers. |

## Methods

### Register(Deserializer)

Registers a new deserializer instance with the garbage collector.

#### Parameters

| Parameters   | Datatype       | Description                            |
| ------------ | -------------- | -------------------------------------- |
| Deserializer | I_Deserializer | The deserializer instance to register. |

### Deregister(Deserializer)

Deregisters a deserializer instance from the garbage collector.

#### Parameters

| Parameters   | Datatype       | Description                              |
| ------------ | -------------- | ---------------------------------------- |
| Deserializer | I_Deserializer | The deserializer instance to deregister. |

### Execute()

Triggers disposal of all registered deserializer instances.
