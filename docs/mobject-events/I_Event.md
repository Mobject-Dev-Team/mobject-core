# I_Event Interface

## Definition

|             |                            |
| ----------- | -------------------------- |
| Namespace   | mobject-events             |
| Library     | mobject-events             |
| Inheritance | \_\_System.IQueryInterface |
| Implements  |                            |

## Remarks

The I_Event interface should be implemented by an object if it is to be passed to event handlers. There are no requirements to be able to implement the I_Event interface. Handlers should use this interface as a base to query against using \_\_QUERYINTERFACE.

## Example

In the example below, a new Event object has been created which implements the I_OnValueChangedEvent. This I_OnValueChangedEvent extends I_Event and as such can be used to downcast the event.

New OnValueChangedEvent

```declaration
FUNCTION_BLOCK OnValueChangedEvent IMPLEMENTS I_OnValueChangedEvent
VAR
  _newValue : INT;
END_VAR
```

```body
  // ...
```

```declaration
PROPERTY PUBLIC NewValue : INT
```

```body
// Get
NewValue := _newValue;
```

New I_OnValueChangedEvent

```declaration
INTERFACE I_OnValueChangedEvent EXTENDS I_Event

PROPERTY PUBLIC NewValue : INT
```

New OnValueChangedEventHandler

```declaration
FUNCTION_BLOCK OnValueChangedEventHandler IMPLEMENTS I_EventHandler
VAR
END_VAR
```

```body
// ...
```

```declaration
METHOD PUBLIC HandleEvent
VAR_INPUT
	Event : I_Event;
END_VAR
VAR
    onValueChangeEvent : I_OnValueChangedEvent;
    newValue : INT;
END_VAR
```

```body
// first check to see if the event passed in is a I_OnValueChangedEvent.
IF NOT __QUERYINTERFACE(Event,onValueChangeEvent) THEN
    RETURN; // if not then return
END_IF

// if it is then you can use it directly as __QueryInterface automatically completes the conversion.
newValue := onValueChangeEvent.NewValue;
```
