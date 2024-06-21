# EventEmitter Class

## Definition

|             |                                                      |
| ----------- | ---------------------------------------------------- |
| Namespace   | mobject-events                                       |
| Library     | mobject-events                                       |
| Inheritance | [Disposable](./mobject-disposable/Disposable.md)     |
| Implements  | [I_Disposable](./mobject-disposable/I_Disposable.md) |

## Remarks

The EventEmitter Class is a utility class that allows objects to emit events and for other objects to listen for those events and react accordingly. It is designed to be a lightweight, easy-to-use implementation of the Observer Pattern.

## Example

```declaration
PROGRAM Main
VAR
  eventEmitter : EventEmitter;
  eventHandler : DemoEventHandler; // object implementing I_EventHandler
  event : DemoEvent; // object implementing I_Event
END_VAR
```

```body
// an event can be subscribed to by passing in the name of the event
// and a handler who implements the I_EventHandler interface.
eventEmitter.OnEvent('onTriggered', eventHandler);

// events can then be emitted using either name and event
// here the eventHandlers who are subscribed to 'onTriggered' will be
// called and passed the event given to the eventEmitter.
eventEmitter.Emit('onTriggered',event);

// events can be unsubscribed in the same manor
eventEmitter.OffEvent('onTriggered', eventHandler);
```

## Methods

### Clear()

Removes all event handlers from the EventEmitter.

#### Parameters

N/A

#### Return

N/A

#### Usage

```example
eventEmitter.Clear();
```

### Emit(EventName, Event)

Emits an event with the given name and data.

#### Parameters

| Parameters | Datatype                               | Description                         |
| ---------- | -------------------------------------- | ----------------------------------- |
| EventName  | T_MAXSTRING                            | The name of the event.              |
| Event      | [I_Event](./mobject-events/I_Event.md) | The data associated with the event. |

#### Return

N/A

#### Usage

```example
eventEmitter.Emit('onTriggered',event);
```

### OnEvent(EventName, EventHandler)

Registers an event handler for the given event name.

#### Parameters

| Parameters   | Datatype                                             | Description                    |
| ------------ | ---------------------------------------------------- | ------------------------------ |
| EventName    | T_MAXSTRING                                          | The name of the event.         |
| EventHandler | [I_EventHandler](./mobject-events/I_EventHandler.md) | The event handler to register. |

#### Return

N/A

#### Usage

```example
eventEmitter.OnEvent('OnValueChange', eventHandler);
```

### OnceEvent(EventName, EventHandler)

Registers an event handler for the given event name which is triggered only once.

#### Parameters

| Parameters   | Datatype                                             | Description                    |
| ------------ | ---------------------------------------------------- | ------------------------------ |
| EventName    | T_MAXSTRING                                          | The name of the event.         |
| EventHandler | [I_EventHandler](./mobject-events/I_EventHandler.md) | The event handler to register. |

#### Return

N/A

#### Usage

```example
eventEmitter.OnceEvent('OnValueChange', eventHandler);
```

### OffEvent(EventName, EventHandler)

Unregisters an event handler for the given event name.

#### Parameters

| Parameters   | Datatype                                             | Description                      |
| ------------ | ---------------------------------------------------- | -------------------------------- |
| EventName    | T_MAXSTRING                                          | The name of the event.           |
| EventHandler | [I_EventHandler](./mobject-events/I_EventHandler.md) | The event handler to unregister. |

#### Return

N/A

#### Usage

```example
eventEmitter.OffEvent('OnValueChange', eventHandler);
```

## Implementation Example

The example below will show you how you can add an EventEmitter to your own object so that other objects may interact with it and react to events. We will create a simple object which will emit an event every time a .Execute() method is called.

1. Start by creating MyObject Function Block.

2. Our class should implement the [I_EventTarget](./mobject-events/I_EventTarget.md) interface as good practice. This allows other objects to know it supports events in this way.

```declaration
FUNCTION_BLOCK MyObject IMPLEMENTS I_EventTarget
VAR
  eventEmitter : EventEmitter;
END_VAR
```

```body
//... no code should go here.
```

>

```declaration
METHOD OnEvent
VAR_INPUT
  EventName : T_MAXSTRING;
  EventHandler : I_EventHandler;
END_VAR
```

```body
eventEmitter.OnEvent(EventName, Event);
```

4. Next create a method called OffEvent. This will allow people to unregister a handler from your object.

```declaration
METHOD OffEvent
VAR_INPUT
  EventName : T_MAXSTRING;
  EventHandler : I_EventHandler;
END_VAR
```

```body
eventEmitter.OffEvent(EventName, Event);
```

5. Finally create a method called Execute. In our test, this is what shall trigger the event. In this example we are not going to pass in an event object as this will be covered in the later examples.

```declaration
METHOD Execute
VAR_INPUT
END_VAR
```

```body
eventEmitter.Emit('OnExecute', 0);
```

<!-- tabs:end -->
