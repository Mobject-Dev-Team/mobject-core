# JsonDomParser Class

## Definition

|             |                                                                                                                                           |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| Namespace   | mobject-json                                                                                                                              |
| Library     | mobject-json                                                                                                                              |
| Inheritance | [FB_JsonDynDomParser](https://infosys.beckhoff.com/english.php?content=../content/1033/tf6701_tc3_iot_communication_mqtt/8101725835.html) |
| Implements  | N/A                                                                                                                                       |

## Remarks

The JsonDomParser Class is an extension to the current TwinCAT implementation of FB_JsonDynDomParser. This class adds functionality such as the ability to read from the JSON document using [JSONPath Syntax](https://support.smartbear.com/alertsite/docs/monitors/api/endpoint/jsonpath.html).

## Example

```declaration
PROGRAM Main
VAR
  jsonParser : JsonDomParser;
  json : T_MAXSTRING := '{"level1" : {"level2" : {"level3" : {"level4" : 123, "myArray" : ["a","b","c"]}}}}';
  result : DINT;
  newString : STRING := 'd';
  successful : BOOL;
END_VAR
```

```body
// first parse the document
jsonParser.ParseDocument(json);

// use the new "TryRead" method to read values using JSONPath Syntax
successful := jsonParser.TryRead('.level1.level2.level3.level4', result);
// successful = true
// result := 123

successful := jsonParser.TryModify('.level1.level2.level3.myArray[2]', newString);
json := jsonParser.GetDocument();
// successful = true
// json = '{"level1" : {"level2" : {"level3" : {"level4" : 123, "myArray" : ["a","b","d"]}}}}';
```

## Methods

### TryLocate(Path, Destination)

Tries to resolve the json path specified to a SJsonValue.

#### Parameters

| Parameters  | Datatype    | Description                                                  |
| ----------- | ----------- | ------------------------------------------------------------ |
| Path        | T_MAXSTRING | The path of the value specified in JSONPath Syntax           |
| Destination | REFERENCE TO SJsonValue | The symbol used as the destination if the read is successful |

#### Return

| Datatype | Description                             |
| -------- | --------------------------------------- |
| BOOL     | Returns true if the get was successful |

#### Usage

```example
// {"myInt" : 123}';
read := jsonParser.TryLocate('.myInt', location);  // location = pointer to json value 123, read = true
```

### TryModify(Path, Source)

Tries to modify the value at the path specified. The modify will fail if the path does not already exist.

#### Parameters

| Parameters | Datatype    | Description                                        |
| ---------- | ----------- | -------------------------------------------------- |
| Path       | T_MAXSTRING | The path of the value specified in JSONPath Syntax |
| Source     | ANY         | The symbol used as the source data                 |

#### Return

| Datatype | Description                               |
| -------- | ----------------------------------------- |
| BOOL     | Returns true if the modify was successful |

#### Usage

```example
// {"myInt" : 123}';
newValue := 456;
modified := jsonParser.TryModify('.myInt', newValue);  // {"myInt" : 456}, modified = true
```

### TryRead(Path, Destination)

Tries to read the value at the path specified.

#### Parameters

| Parameters  | Datatype    | Description                                                  |
| ----------- | ----------- | ------------------------------------------------------------ |
| Path        | T_MAXSTRING | The path of the value specified in JSONPath Syntax           |
| Destination | ANY         | The symbol used as the destination if the read is successful |

#### Return

| Datatype | Description                             |
| -------- | --------------------------------------- |
| BOOL     | Returns true if the read was successful |

#### Usage

```example
// {"myInt" : 123}';
read := jsonParser.TryRead('.myInt',result);  // result = 123, read = true
```

### TryWrite(Path, Source)

The TryWrite() method attempts to write a value at the specified path within a JSON document. If the path does not exist, the method will attempt to create the necessary structure in the JSON document to accommodate the value.

#### Parameters

| Parameters | Datatype    | Description                                             |
| ---------- | ----------- | ------------------------------------------------------- |
| Path       | T_MAXSTRING | The path of the value specified in JSONPath Syntax      |
| Source     | ANY         | The data value you want to write to the specified path. |

#### Return

| Datatype | Description                              |
| -------- | ---------------------------------------- |
| BOOL     | Returns true if the write was successful |

#### Usage

```example
// Initial JSON: {"user" : {"name" : "Alice"}}
newValue := 25;
modifiedAge := jsonParser.TryWrite('.user.age', newValue);  // Adds an "age" field to the "user" object

newAddress := '123 Maple St';
modifiedAddress := jsonParser.TryWrite('.user.address.street', newAddress);  // Creates a nested "address" object with a "street" field inside the "user" object

newCity := 'Wonderland';
modifiedCity := jsonParser.TryWrite('.user.address.city', newCity);  // Adds a "city" field to the newly created "address" object

// After the operations, JSON becomes:
// {"user" : {"name" : "Alice", "age" : 25, "address" : {"street" : "123 Maple St", "city" : "Wonderland"}}}
// The 'modifiedAge', 'modifiedAddress', and 'modifiedCity' variables are all set to true.
```
