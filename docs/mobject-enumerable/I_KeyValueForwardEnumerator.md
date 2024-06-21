# I_KeyValueForwardEnumerator Interface

## Definition

|             |                                                                    |
| ----------- | ------------------------------------------------------------------ |
| Namespace   | mobject-enumerable                                                 |
| Library     | mobject-enumerable                                                 |
| Inheritance | [I_ForwardEnumerator](./mobject-enumerable/I_ForwardEnumerator.md) |
| Implements  |                                                                    |

## Remarks

The I_KeyValueForwardEnumerator interface should be implemented by all enumerators created to enumerate in a single direction over a key value dataset.

## Properties

### Key

Returns the current key of the key value pair.

#### Return

| Datatype    | Description                            |
| ----------- | -------------------------------------- |
| T_MAXSTRING | The current key of the key value pair. |
