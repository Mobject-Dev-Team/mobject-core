# I_DeserializerGarbageCollector Interface

## Definition

|             |                            |
| ----------- | -------------------------- |
| Namespace   | mobject-serialization      |
| Library     | mobject-serialization      |
| Inheritance | \_\_SYSTEM.IQueryInterface |
| Implements  |                            |

## Remarks

The `I_DeserializerGarbageCollector` interface is designed to manage the lifecycle of deserializers within the system. It provides mechanisms to register and deregister deserializer instances, ensuring proper garbage collection and resource management.

## Methods

### Deregister(Deserializer)

Deregisters a deserializer from the garbage collector, removing it from the management scope.

#### Parameters

| Parameters   | Datatype       | Description                              |
| ------------ | -------------- | ---------------------------------------- |
| Deserializer | I_Deserializer | The deserializer instance to deregister. |

### Register(Deserializer)

Registers a deserializer with the garbage collector, adding it to the management scope.

#### Parameters

| Parameters   | Datatype       | Description                            |
| ------------ | -------------- | -------------------------------------- |
| Deserializer | I_Deserializer | The deserializer instance to register. |
