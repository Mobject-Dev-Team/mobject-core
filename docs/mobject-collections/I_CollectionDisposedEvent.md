# I_CollectionDisposedEvent Interface

## Definition

|             |                                        |
| ----------- | -------------------------------------- |
| Namespace   | mobject-collections                    |
| Library     | mobject-collections                    |
| Inheritance | [I_Event](./mobject-events/I_Event.md) |
| Implements  |                                        |

## Remarks

The I_CollectionDisposedEvent is an event emitted by the [I_Collection](./mobject-collections/I_Collection.md) interface.

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
    collectionDisposedEvent : I_CollectionDisposedEvent;
    originator : I_LinkedList;
END_VAR
```

```body
IF __QUERYINTERFACE(Event, collectionDisposedEvent) THEN
    // the received event was I_CollectionDisposedEvent.  You can now use the interface
    // to extract which collection raised it
    // ...
    originator := collectionDisposedEvent.Target;
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
