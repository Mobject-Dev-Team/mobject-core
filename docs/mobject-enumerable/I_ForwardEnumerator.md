# I_ForwardEnumerator Interface

## Definition

|             |                                                      |
| ----------- | ---------------------------------------------------- |
| Namespace   | mobject-enumerable                                   |
| Library     | mobject-enumerable                                   |
| Inheritance | [I_Disposable](./mobject-disposable/I_Disposable.md) |
| Implements  |                                                      |

## Remarks

The I_ForwardEnumerator interface should be implemented by all enumerators created to enumerate in a single direction over a dataset.

## Methods

### MoveNext()

Moves the enumerator to the next item. Enumerators start before the first item, so you must call MoveNext() once at the start of reading. This is a .net style of enumerator which allows easy use in While Loops.

#### Parameters

N/A

#### Return

| Datatype | Description                                                |
| -------- | ---------------------------------------------------------- |
| BOOL     | Returns true if the enumerator moved to a valid next value |

#### Usage

```example
enumerator := dataset.GetEnumerator();

// the enumerator follows the .net style, which means you must call MoveNext once to
// move to the first item.  This allows you to directly use the enumerator in a while
// loop.
WHILE enumerator.MoveNext() DO
	enumerator.TryGet(data);
END_WHILE;

// you must dispose enumerators as they are new objects.
enumerator.Dispose();
```

### Reset()

Resets the enumerator to before the first item.

#### Parameters

N/A

#### Return

N/A

### TryGet(Destination)

Tries to return the data held at the current location in the enumerator to the destination symbol.

#### Parameters

| Parameters  | Datatype | Description                                      |
| ----------- | -------- | ------------------------------------------------ |
| Destination | ANY      | The destination used to store the returned data. |

#### Return

| Datatype | Description                           |
| -------- | ------------------------------------- |
| BOOL     | Returns true if the data was returned |

#### Usage

```example
enumerator := dataset.GetEnumerator();

// the enumerator follows the .net style, which means you must call MoveNext once to
// move to the first item.  This allows you to directly use the enumerator in a while
// loop.
WHILE enumerator.MoveNext() DO
	enumerator.TryGet(data);
END_WHILE;

// you must dispose enumerators as they are new objects.
enumerator.Dispose();
```

### TryGetTo(DestinationAddress, DestinationSize)

Tries to return the data held at the current location in the enumerator to the destination symbol using address and size.

#### Parameters

| Parameters         | Datatype | Description                                              |
| ------------------ | -------- | -------------------------------------------------------- |
| DestinationAddress | PVOID    | The destination address used to store the returned data. |
| DestinationSize    | UDINT    | The destination size used to store the returned data.    |

#### Return

| Datatype | Description                           |
| -------- | ------------------------------------- |
| BOOL     | Returns true if the data was returned |

#### Usage

```example
enumerator := dataset.GetEnumerator();

// the enumerator follows the .net style, which means you must call MoveNext once to
// move to the first item.  This allows you to directly use the enumerator in a while
// loop.
WHILE enumerator.MoveNext() DO
	enumerator.TryGetTo(ADR(data),SIZEOF(data));
END_WHILE;

// you must dispose enumerators as they are new objects.
enumerator.Dispose();
```

## Properties

### IsValid

Returns if the enumerator is valid. An enumerator will become invalid if the underlying data was changed after the enumerator was created.

#### Return

| Datatype | Description                       |
| -------- | --------------------------------- |
| BOOL     | True indicates a valid enumerator |
