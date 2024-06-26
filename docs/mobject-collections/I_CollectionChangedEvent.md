# I_CollectionChangedEvent Interface

## Definition

|             |                                        |
| ----------- | -------------------------------------- |
| Namespace   | mobject-collections                    |
| Library     | mobject-collections                    |
| Inheritance | [I_Event](./mobject-events/I_Event.md) |
| Implements  |                                        |

## Remarks

The I_CollectionChangedEvent is an event emitted by any collection implementing the [I_Collection](./mobject-collections/I_Collection.md) interface.

## Example

```declaration
FUNCTION_BLOCK MyHandler IMPLEMENTS I_EventHandler
VAR
END_VAR
```

```body
//... no code should go here.
```

```declaration
METHOD HandleEvent
VAR_INPUT
    Event : I_Event;
END_VAR
VAR
    collectionChangedEvent : I_CollectionChangedEvent;
    originator : I_Collection;
END_VAR
```

```body
IF __QUERYINTERFACE(Event, collectionChangedEvent) THEN
    // the received event was I_CollectionChangedEvent.  You can now use the interface
    // to extract which collection raised it
    // ...
    originator := collectionChangedEvent.Target;
END_IF

// other event checks can follow here..
// ...
```

## Properties

### Target

Returns the collection who raised the event.

#### Return

| Datatype                                              | Description                         |
| ----------------------------------------------------- | ----------------------------------- |
| [I_Collection](./mobject-collections/I_Collection.md) | The collection who raised the event |
