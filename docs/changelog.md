# Changelog

## v0.1.0-beta

- Initial commit, with the following libs included.
  - mobject-collections (v1.3.0)
  - mobject-commands (v0.2.0)
  - mobject-constants-datatype-limits (v1.0.0)
  - mobject-datatypes (v0.10.0)
  - mobject-deserialization (v0.3.0)
  - mobject-disposable (v1.1.1)
  - mobject-enumerable (v1.2.0)
  - mobject-errors (v0.3.0)
  - mobject-events (v1.1.0)
  - mobject-json (v1.6.0)
  - mobject-serialization (v0.5.0)

# Pre-merge History

## mobject-disposable v1.1.1-beta

- Minor style change, adding public to Dispose method

## mobject-disposable v1.1.0-beta

- Changed to make compatible with TwinCAT 4026 as the line \_\_DELETE(THIS) is no longer supported.

## mobject-disposable v1.0.0-beta

- Changed status from alpha to beta.
- Updated documentation to support dark mode.
- Library built using 4024.53.

## mobject-disposable v0.3.1-alpha

- Renamed the test suite.
- Removed Mock classes that used OnDispose method.
- Fixed typos and text.
- Fixed test project to use specific version (0.3.1) of library.

## mobject-disposable v0.3.0-alpha

- Removed OnDispose. Due to new information being provided in regards to how FB_exit operates it is no longer possible to implement the OnDispose method in this way. FB_exit does not follow the same rules as an inherited method, and as such would have only called OnDispose at the point when the disposable abstract class was destroyed, NOT at the point that a child class is destroyed. This is a subtle issue which is worth removing this functionality for. If left in it could have resulted in some very hard to find bugs in the user code.

## mobject-disposable v0.2.1-alpha

- Removed ABSTRACT from Disposable OnDispose. This removes the requirement from the end user to implement the OnDispose if the child class has no requirement for it. You would still look to extend from Disposable to handle the usual lifecycle of disposing and deleting of the object.

## mobject-collections v1.3.0-beta

- Updated to support mobject-disposable v1.1.1
- Updated to support mobject-enumerable v1.2.0
- Updated to support mobject-events v1.1.0

## mobject-collections v1.2.0-beta

- Added OrderedDictionary, which preserves the order of added items when using enumerators
- Added IsEmpty to I_Collection

## mobject-collections v1.1.0-beta

- Updated to support mobject-enumerable v1.1.0-beta.
- Added the Reset method.
- Dictionary to support I_KeyValueEnumerable.
- Dictionary enumerator to support I_KeyValueForwardEnumerator.
- Enumerators will auto dispose on parent dispose.

## mobject-collections v1.0.0-beta

- Changed status from alpha to beta.
- Updated documentation to support dark mode.
- Library built using 4024.53.
- Updated to support mobject-disposable v1.0.0-beta.
- Updated to support mobject-enumerable v1.0.0-beta.
- Updated to support mobject-events v1.0.0-beta.
- Documentation correction.

## mobject-collections v0.9.0-alpha

- Documentation update

!> This update contains the following breaking changes.

- Method calls which perform an action and return TRUE or FALSE based on their success are now prefixed with "Try". For example, list.CopyTo() -> list.TryCopyTo(). This is to improve their readability and promote their use in IF statements.

## mobject-collections v0.8.1-alpha

- Bugfix Dictionary ForwardEnumerator not returning correct element when MoveNext() was called.
- Library built using 4024.53.

## mobject-collections v0.8.0-alpha

- Added Dictionary Class.
- Bugfix Events were not implemented correctly on the ListEnumerator. These have been added.
- Converted referenced libraries to actual libraries rather than placeholders
- Added I_CollectionNode as a base to I_LinkedListNode, I_ListNode and I_DictionaryNode.

!> This update contains the following breaking changes.

- Removed Reset from enumerators (as this is not a commonly implemented method)
- FB_init of ListForwardEnumerator has argument List changed to Parent.

## mobject-collections v0.7.0-alpha

- Added List and ListForwardEnumerator Classes.
- Changed I_Collection to extend from I_EventEmitter.

!> This update contains the following breaking changes.

- I_Collection.Count is now DINT.
- Individual OnChanged and OnDisposed event classes have been removed and replaced by generic collection events.
- Added mobject-enumerable 0.1.0.
- Changed all Destination to DestinationAddress on arguments of PVOID.

## mobject-collections v0.6.0-alpha

- Library built using 4024.44.
- Queue and Stack support events 'OnChanged' and 'OnDisposed'.

!> This update contains the following breaking changes.

- LinkedListNode methods Get and GetTo have been renamed to TryGet and TryGetTo.
- LinkedList events 'OnLinkedListChanged' and 'OnLinkedListDisposed' renamed to 'OnChanged' and 'OnDisposed'. This will allow all collections to use the same name and for the event emitter to move to the I_Collection interface on a future release.
- Removed Collection but kept I_Collection

## mobject-collections v0.5.0-alpha

- Added Collection
- Added further tests for collection and enumerators

## mobject-collections v0.4.0-alpha

- Remove I_Enumerable interface to mobject-enumerable
- Added mobject-enumerable 0.0.0

## mobject-collections v0.3.0-alpha

- Added I_Enumerable interface
- Added I_Collection interface
- Added I_Queue interface
- Added I_Stack interface

## mobject-collections v0.2.1-alpha

- Updated to support mobject-disposable v0.3.1-alpha
- Updated to support mobject-events v0.4.1-alpha

## mobject-collections v0.2.0-alpha

- Updated to support mobject-disposable v0.3.0-alpha
- Updated to support mobject-events v0.4.0-alpha
- Added tests for enumerators
- All tests now passing

## mobject-collections v0.1.0-alpha

### Queue

- Added support for CopyTo and CopyToLocation, which matches the feature on LinkedList.

### NEW - Stack

- Added the Stack (fifo) class.

## mobject-collections v0.0.0-alpha

- Initial commit
- Supports LinkedList, ForwardEnumerators, Queue's.

## mobject-commands v0.2.0-alpha

- Updated to support mobject-disposable v1.1.1

## mobject-commands v0.1.0-alpha

- Updated documentation to support dark mode.
- Library built using 4024.53.
- Updated to support mobject-disposable v1.0.0-beta.

!> This update contains the following breaking changes.

- I_Command extends from I_Disposable.

## mobject-commands v0.0.1-alpha

Initial

## mobject-constants-datatype-limits - v0.1.0-alpha

- First alpha release

## mobject-datatypes v0.10.0-alpha

- Added support for interfaces

## mobject-datatypes v0.9.0-alpha

- Correctly serializes structure and enums in order they are added. (i.e. using OrderedDictionary)

## mobject-datatypes v0.8.0-alpha

- \_BIT datatype added
- added 2 memory operations, WriteBitToBoolOperation and WriteBoolToBitOperation
- updated to support mobject-deserialization v0.3.0
- Updated to support mobject-collections v1.3.0
- Updated to support mobject-disposable v1.1.1
- Updated to support mobject-enumerable v1.2.0
- Updated to support mobject-errors v0.3.0
- Updated to support mobject-events v1.1.0
- Updated to support mobject-serialization v0.5.0
- swapped values to reference to, so that they can be used directly in functions

## mobject-datatypes v0.7.0-alpha

- updated to support mobject-deserialization v0.2.0
- updated to support mobject-collections v1.2.0
- added interface datatype base

## mobject-datatypes v0.6.0-alpha

- finished / added TryCopyFrom on all datatypes.
- added IsUserDefined property to I_Datatype to assist with conversion
- I_StructuredDatatype now no longer has direct access to TryGetMemberByName (reason, see below)
- I_StructuredDatatype now extends I_HostStructureMembers which gives access to Members
- added 2 memory operations, MemCopyOperation and SafeMemCopyOperation

## mobject-datatypes v0.5.0-alpha

- bug fix TryDeserialize was always returning false on Enums
- moved primitives back to library, this reduces coupling.

## mobject-datatypes v0.4.0-alpha

- removed basic datatypes to their own library. mobject-basic-datatyps.
- renamed GetPrimitiveByTypeName in Datatypes and I_Datatypes
- completed support for enums
- added tests for base types

## mobject-datatypes v0.3.0-alpha

- updated Name to typeName on datatype base and serialization
- LREAL and REAL are now Numeric
- updated to support the new mobject-constants-datatype-limits v1.0.0
- Ubound and Lbound now MinValue and MaxValue in both class and serialization

## mobject-datatypes v0.2.0-alpha

- mobject-types change name to mobject-datatypes
- SerializeTypeWith refactored the following:
  - baseType -> baseDatatype
  - datatype -> name
  - isFloat added
- DatatypeBase has Datatype renamed to Name
- TryResolveAsAliasType renamed to TryResolveAsAliasDatatype
- TryResolveAsEnumType renamed to TryResolveAsEnumDatatype
- TryResolveAsStructuredType renamed to TryResolveAsStructuredDatatype
- Datatypes now supports adding enums
- Alias and Enums method names changed from Type to Datatype

## mobject-datatypes v0.1.2-alpha

- Corrected copy paste error, in which ULINT and UWORD were being treated as LINT when their bounds were serialized.

## mobject-datatypes v0.1.1-alpha

- Added mobject-converters 1.1.0
- Added Accept method to Datatypes to allow visitors
- Added I_EventEmitter to I_Datatypes
- Added event "OnDatatypeAdded" to Datatypes
- Added upper and lower bounds to integer datatypes
- Added new IntegerDatatypeBase
- Added IsSigned to integer datatypes
- Added enum datatype and tests

## mobject-datatypes v0.1.0-alpha

- Initial

## mobject-deserialization v0.3.0-alpha

- Integrated deserialization errors in to deserialization feedback
- Added custom deserialization error
- Added support for mobject-collections v1.3.0
- Added support for mobject-disposable v1.1.1
- Added support for mobject-enumerable v1.2.0
- Added support for mobject-errors v0.3.0
- Added support for mobject-serialization v0.5.0
- Removed mobject-json from tests and replaced with MockJsonSeralizer

## mobject-deserialization v0.2.0-alpha

- Added support for mobject-collections v1.2.0

## mobject-deserialization v0.1.0-alpha

- Initial deserializer code taken from v0.3.0
- Added I_DeserializerObjectForwardEnumerator
- Added I_DeserializerArrayForwardEnumerator
- Added DeserializerFeedback and I_DeserializerFeedback
- Added I_DeserializerFeedbackVisitor

!> This update contains the following breaking changes to the code taken from mobject-serialization v0.3.0.

- I_Deserializer additions, Must now support the following added methods.
  - GetArrayEnumerator
  - GetObjectEnumerator
  - GetObject
- Renamed the GetKey to GetKeyObject
- TryDeserializeFrom now uses an I_DeserializerFeedback to report back a reason if it fails
- Renamed TryGetObject to TryDeserializeToObject
- Renamed TryGetKeyObject to TryDeserializeKeyToObject

## mobject-enumeration v1.2.0-beta

- Updated to support mobject-disposable v1.1.1
- Minor style change

## mobject-enumeration v1.1.0-beta

- Added reset to enumerators.
- Added I_KeyValueEnumerable for use with collections such as dictionaries.
- Added I_KeyValueForwardEnumerator

## mobject-enumeration v1.0.0-beta

- Changed status from alpha to beta.
- Updated documentation to support dark mode.
- Library built using 4024.53.
- Added unit tests.
- Updated to support mobject-disposable v1.0.0-beta.

## mobject-enumeration v0.1.0-alpha

- Refactor of I_ForwardEnumerator TryGetTo method.

## mobject-enumeration v0.0.0-alpha

- Alpha release.

## mobject-errors v0.3.0-alpha

- Updated to support mobject-disposable v1.1.1
- Updated to support mobject-serialization v1.5.0
- Removed mobject-json from tests and replaced with MockJsonSeralizer

## mobject-errors v0.2.0-alpha

- Updated interface I_Error to support ErrorType
- Updated interface I_Error to support I_Serializable
- Updated interface to support IsSameAs method.
- Added Error Abstract Base.
- Error is now disposable
- Added I_ErrorVisitor
- Added Accept to Error and I_Error

## mobject-errors v0.1.0-alpha

- First alpha release

## mobject-events v1.1.0-beta

- Updated to support mobject-disposable v1.1.1
- Minor style change

## mobject-events v1.0.0-beta

- Changed status from alpha to beta.
- Updated documentation to support dark mode.
- Library built using 4024.53.
- Added unit tests.
- Updated to support mobject-disposable v1.0.0-beta.

## mobject-events v0.4.1-alpha

- Updated to support mobject-disposable v0.3.1-alpha

## mobject-events v0.4.0-alpha

- Updated to support mobject-disposable v0.3.0-alpha

## mobject-json v1.6.0-beta

- Added support for mobject-deserialization v0.3.0
- Added support for mobject-disposable v1.1.1
- Added support for mobject-errors v0.3.0
- Added support for mobject-events v1.1.0
- Added support for mobject-serialization v0.5.0

## mobject-json v1.5.0-beta

- Updated to support mobject-deserialization v0.2.0-alpha

## mobject-json v1.4.0-beta

- Updated to support mobject-converters v1.0.2-beta.
- Corrected issue with TwinCAT REAL serialization. JsonSaxWriter did not correctly support MAX value real, so JsonSerializer now converts to LREAL first. Only issue is you now gain more decimal places.

## mobject-json v1.3.0-beta

- Updated to support mobject-serialization v0.4.0-alpha.
- Updated to support mobject-deserialization v0.1.0-alpha.
- Added JsonDeserializerArrayForwardEnumerator
- Added JsonDeserializerObjectForwardEnumerator
- Enumerators all auto dispose, same as mobject-collections.

## mobject-json v1.2.0-beta

- Updated to support mobject-serialization v0.3.0-alpha.
- Added JsonSeralizer.AddObject
- Added JsonSeralizer.AddKeyObject
- Added JsonDeserializer + tests

!> This update contains the following breaking changes.

- JsonSeralizer.AddKeyRawObject renamed to .AddKeyRawJson
- JsonSeralizer.AddRawObject renamed to AddRawJson

## mobject-json v1.1.0-beta

- Updated to support mobject-serialization v0.1.0-alpha.
- Added JsonSerializer

## mobject-json v1.0.1-beta

- Updated to support mobject-converters v1.0.1-beta.
- Bugfix with JsonDomParser writing Int and Uint64.
- Added explicit conversion to remove warning message.

## mobject-json v1.0.0-beta

- Changed status from alpha to beta.
- Updated documentation to support dark mode.
- Library built using 4024.53.
- Updated to support mobject-disposable v1.0.0-beta.
- Updated to support mobject-converters v1.0.0-beta.

## mobject-json v0.3.0-alpha

- Added TryLocate() method which attempts to resolve the path into an SJsonValue which can be used with the parser.

## mobject-json v0.2.0-alpha

- Added TryWrite() method which attempts to write a value at the specified path within a JSON document. If the path does not exist, the method will attempt to create the necessary structure in the JSON document to accommodate the value.

## mobject-json v0.1.1-alpha

- Refactored Json Path Syntax Parsing to it's own class. It's now possible to parse paths using an I_JsonPathVisitor.
  This will allow future expansion to allow for writing to json using the path.

## mobject-json v0.1.0-alpha

- Updated to 4024.47
- Updated to use mobject-converters 0.1.1
- Added TryModify(), this method will modify a value if it exists

## mobject-json v0.0.0-alpha

- First alpha release

## mobject-serialization v0.5.0-alpha

- Updated to support mobject-disposable v1.1.1

## mobject-serialization v0.4.0-alpha

!> This update contains the following breaking changes.

- All deserializer code moved to mobject-deserializer

## mobject-serialization v0.3.0-alpha

!> This update contains the following breaking changes.

- Added Clone to I_Deserializer interface.
- Renamed TryDeserializeKeyToObject and TryDeserializeToObject to TryGetKeyObject and TryGetObject inside the I_Deserializer interface.

## mobject-serialization v0.2.0-alpha

- Added I_Deserializer and I_Deserializable
- DeserializerGarbageCollector class. Common component used when writing your own deserializers for managing the life cycle of child nodes.
- Added dependency on mobject-collections 1.0.0.

!> This update contains the following breaking changes.

- Added AddObject and AddKeyObject to I_Seralizer, classes already created as I_Seralizer will need to implement two new methods. This is simple to add as you will only need to pass the same class back to the object. See mobject-json seralizer for an example.

## mobject-serialization v0.1.0-alpha

- Initial
