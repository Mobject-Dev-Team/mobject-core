# I_KeyValueEnumerable Interface

## Definition

|             |                            |
| ----------- | -------------------------- |
| Namespace   | mobject-enumerable         |
| Library     | mobject-enumerable         |
| Inheritance | \_\_System.IQueryInterface |
| Implements  |                            |

## Remarks

The I_KeyValueEnumerable interface contains common methods and properties found on objects which are enumerable which hold data as key value pairs.

## Methods

### GetKeyValueEnumerator()

Returns a forward enumerator for the enumerable object. More information on the enumerators can be found [here](I_KeyValueForwardEnumerator.md)

!> Enumerators are \_\_NEW objects, which means you must dispose of any enumerators you make once you are finished using them. Failure to do so will result in a memory leak.

#### Parameters

N/A

#### Return

| Datatype                                                                           | Description                                                           |
| ---------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| [I_KeyValueForwardEnumerator](./mobject-enumerable/I_KeyValueForwardEnumerator.md) | The method will return a forward enumerator for the enumerable object |

#### Usage

```declaration
enumerator : I_KeyValueForwardEnumerator;
dataset : Dictionary;
```

```body
enumerator := dataset.GetKeyValueEnumerator();

// the enumerator follows the .net style, which means you must call MoveNext once to
// move to the first item.  This allows you to directly use the enumerator in a while
// loop.
WHILE enumerator.MoveNext() DO
	enumerator.TryGet(data);
END_WHILE;

// you must dispose enumerators as they are new objects.
enumerator.Dispose();
```
