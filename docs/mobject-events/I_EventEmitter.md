# I_EventEmitter Interface

## Definition

|             |                            |
| ----------- | -------------------------- |
| Namespace   | mobject-events             |
| Library     | mobject-events             |
| Inheritance | \_\_System.IQueryInterface |
| Implements  |                            |

## Remarks

The I_EventEmitter interface is a common interface which should be implemented by any class able to emit events. Three basic methods should be implemented. OnEvent and OffEvent used to subscribe and unsubscribe handlers to events, and one further method OnceEvent which will automatically unsubscribe the event after being triggered.

## Methods

### OnEvent(Event)

#### Parameters

| Parameters   | Datatype                                             |
| ------------ | ---------------------------------------------------- |
| EventName    | T_MAXSTRING                                          |
| EventHandler | [I_EventHandler](./mobject-events/I_EventHandler.md) |

#### Return

N/A

### OnceEvent(Event)

#### Parameters

| Parameters   | Datatype                                             |
| ------------ | ---------------------------------------------------- |
| EventName    | T_MAXSTRING                                          |
| EventHandler | [I_EventHandler](./mobject-events/I_EventHandler.md) |

#### Return

N/A

### OffEvent(Event)

#### Parameters

| Parameters   | Datatype                                             |
| ------------ | ---------------------------------------------------- |
| EventName    | T_MAXSTRING                                          |
| EventHandler | [I_EventHandler](./mobject-events/I_EventHandler.md) |

#### Return

N/A
