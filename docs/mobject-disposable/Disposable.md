# Disposable Class

## Definition

|             |                                                      |
| ----------- | ---------------------------------------------------- |
| Namespace   | mobject-disposable                                   |
| Library     | mobject-disposable                                   |
| Inheritance | None                                                 |
| Implements  | [I_Disposable](./mobject-disposable/I_Disposable.md) |

## Remarks

The Disposable Abstract Class is a utility class that allows objects to handle being destroyed in a consistent manner.

## Example

```declaration
FUNCTION_BLOCK MyObject EXTENDS Disposable
VAR
END_VAR
```

```body
//... no code should go here.
```

## Methods

### Dispose()

Will trigger the object for deletion.

#### Parameters

N/A

#### Return

N/A

#### Usage

```example
myObject.Dispose()
```
