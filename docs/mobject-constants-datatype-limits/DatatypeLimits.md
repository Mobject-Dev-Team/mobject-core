# DatatypeLimits.GVL

## Boolean Datatypes

| Constant       | type | Value |
| -------------- | ---- | ----- |
| BOOL_MIN_VALUE | BOOL | FALSE |
| BOOL_MAX_VALUE | BOOL | TRUE  |

## Integer Datatypes

| Constant        | type  | Value                      |
| --------------- | ----- | -------------------------- |
| BYTE_MIN_VALUE  | BYTE  | BYTE#0                     |
| BYTE_MAX_VALUE  | BYTE  | BYTE#255                   |
| WORD_MIN_VALUE  | WORD  | WORD#0                     |
| WORD_MAX_VALUE  | WORD  | WORD#65535                 |
| DWORD_MIN_VALUE | DWORD | DWORD#0                    |
| DWORD_MAX_VALUE | DWORD | DWORD#4294967295           |
| LWORD_MIN_VALUE | LWORD | LWORD#0                    |
| LWORD_MAX_VALUE | LWORD | LWORD#18446744073709551615 |
| SINT_MIN_VALUE  | SINT  | SINT#-128                  |
| SINT_MAX_VALUE  | SINT  | SINT#127                   |
| USINT_MIN_VALUE | USINT | USINT#0                    |
| USINT_MAX_VALUE | USINT | USINT#255                  |
| INT_MIN_VALUE   | INT   | INT#-32768                 |
| INT_MAX_VALUE   | INT   | INT#32767                  |
| UINT_MIN_VALUE  | UINT  | UINT#0                     |
| UINT_MAX_VALUE  | UINT  | UINT#65535                 |
| DINT_MIN_VALUE  | DINT  | DINT#-2147483648           |
| DINT_MAX_VALUE  | DINT  | DINT#2147483647            |
| UDINT_MIN_VALUE | UDINT | UDINT#0                    |
| UDINT_MAX_VALUE | UDINT | UDINT#4294967295           |
| LINT_MIN_VALUE  | LINT  | LINT#-9223372036854775808  |
| LINT_MAX_VALUE  | LINT  | LINT#9223372036854775807   |
| ULINT_MIN_VALUE | ULINT | ULINT#0                    |
| ULINT_MAX_VALUE | ULINT | ULINT#18446744073709551615 |

## Floating-point types

| Constant                 | type  | Value                          |
| ------------------------ | ----- | ------------------------------ |
| REAL_MAX_VALUE           | REAL  | REAL#3.402823E+38              |
| REAL_MIN_VALUE           | REAL  | REAL#-3.402823E+38             |
| REAL_POSITIVE_MIN_VALUE  | REAL  | REAL#1.0E-44                   |
| REAL_NEGATIVE_MIN_VALUE  | REAL  | REAL#-1.0E-44                  |
| LREAL_MAX_VALUE          | LREAL | LREAL#1.7976931348623157E+308  |
| LREAL_MIN_VALUE          | LREAL | LREAL#-1.7976931348623157E+308 |
| LREAL_POSITIVE_MIN_VALUE | LREAL | LREAL#4.94065645841247E-324    |
| LREAL_NEGATIVE_MIN_VALUE | LREAL | LREAL#-4.94065645841247E-324   |

## Time Datatypes

| Constant       | type | Value              |
| -------------- | ---- | ------------------ |
| TIME_MIN_VALUE | TIME | T#0MS              |
| TIME_MAX_VALUE | TIME | T#49D17H2M47S295MS |

## Date

| Constant       | type          | Value                             |
| -------------- | ------------- | --------------------------------- |
| DATE_MIN_VALUE | DATE          | DATE#1970-1-1                     |
| DATE_MAX_VALUE | DATE          | DATE#2106-2-7                     |
| DT_MIN_VALUE   | DATE_AND_TIME | DATE_AND_TIME#1970-1-1-0:0:0      |
| DT_MAX_VALUE   | DATE_AND_TIME | DATE_AND_TIME#2106-02-07-06:28:15 |
| TOD_MIN_VALUE  | TIME_OF_DAY   | TIME_OF_DAY#0:0:0                 |
| TOD_MAX_VALUE  | TIME_OF_DAY   | TIME_OF_DAY#23:59:59.999          |

## Limits of BYTE used for conversions

| Constant                                      | type | Value    |
| --------------------------------------------- | ---- | -------- |
| MAX_VALUE_OF_BYTE_WHICH_CAN_BE_HELD_IN_A_SINT | BYTE | BYTE#127 |

## Limits of WORD used for conversions

| Constant                                       | type | Value      |
| ---------------------------------------------- | ---- | ---------- |
| MAX_VALUE_OF_WORD_WHICH_CAN_BE_HELD_IN_A_BYTE  | WORD | WORD#255   |
| MAX_VALUE_OF_WORD_WHICH_CAN_BE_HELD_IN_A_SINT  | WORD | WORD#127   |
| MAX_VALUE_OF_WORD_WHICH_CAN_BE_HELD_IN_A_INT   | WORD | WORD#32767 |
| MAX_VALUE_OF_WORD_WHICH_CAN_BE_HELD_IN_A_USINT | WORD | WORD#255   |

## Limits of DWORD used for conversions

| Constant                                        | type  | Value            |
| ----------------------------------------------- | ----- | ---------------- |
| MAX_VALUE_OF_DWORD_WHICH_CAN_BE_HELD_IN_A_BYTE  | DWORD | DWORD#255        |
| MAX_VALUE_OF_DWORD_WHICH_CAN_BE_HELD_IN_A_WORD  | DWORD | DWORD#65535      |
| MAX_VALUE_OF_DWORD_WHICH_CAN_BE_HELD_IN_A_SINT  | DWORD | DWORD#127        |
| MAX_VALUE_OF_DWORD_WHICH_CAN_BE_HELD_IN_A_INT   | DWORD | DWORD#32767      |
| MAX_VALUE_OF_DWORD_WHICH_CAN_BE_HELD_IN_A_DINT  | DWORD | DWORD#2147483647 |
| MAX_VALUE_OF_DWORD_WHICH_CAN_BE_HELD_IN_A_USINT | DWORD | DWORD#255        |
| MAX_VALUE_OF_DWORD_WHICH_CAN_BE_HELD_IN_A_UINT  | DWORD | DWORD#65535      |
| MAX_VALUE_OF_DWORD_WHICH_CAN_BE_HELD_IN_A_TOD   | DWORD | DWORD#86399999   |

## Limits of LWORD used for conversions

| Constant                                        | type  | Value                     |
| ----------------------------------------------- | ----- | ------------------------- |
| MAX_VALUE_OF_LWORD_WHICH_CAN_BE_HELD_IN_A_BYTE  | LWORD | LWORD#255                 |
| MAX_VALUE_OF_LWORD_WHICH_CAN_BE_HELD_IN_A_WORD  | LWORD | LWORD#65535               |
| MAX_VALUE_OF_LWORD_WHICH_CAN_BE_HELD_IN_A_DWORD | LWORD | LWORD#4294967295          |
| MAX_VALUE_OF_LWORD_WHICH_CAN_BE_HELD_IN_A_SINT  | LWORD | LWORD#127                 |
| MAX_VALUE_OF_LWORD_WHICH_CAN_BE_HELD_IN_A_INT   | LWORD | LWORD#32767               |
| MAX_VALUE_OF_LWORD_WHICH_CAN_BE_HELD_IN_A_DINT  | LWORD | LWORD#2147483647          |
| MAX_VALUE_OF_LWORD_WHICH_CAN_BE_HELD_IN_A_LINT  | LWORD | LWORD#9223372036854775807 |
| MAX_VALUE_OF_LWORD_WHICH_CAN_BE_HELD_IN_A_USINT | LWORD | LWORD#255                 |
| MAX_VALUE_OF_LWORD_WHICH_CAN_BE_HELD_IN_A_UINT  | LWORD | LWORD#65535               |
| MAX_VALUE_OF_LWORD_WHICH_CAN_BE_HELD_IN_A_UDINT | LWORD | LWORD#4294967295          |
| MAX_VALUE_OF_LWORD_WHICH_CAN_BE_HELD_IN_A_TIME  | LWORD | LWORD#4294967295          |
| MAX_VALUE_OF_LWORD_WHICH_CAN_BE_HELD_IN_A_TOD   | LWORD | LWORD#86399999            |
| MAX_VALUE_OF_LWORD_WHICH_CAN_BE_HELD_IN_A_DATE  | LWORD | LWORD#4294967295          |
| MAX_VALUE_OF_LWORD_WHICH_CAN_BE_HELD_IN_A_DT    | LWORD | LWORD#4294967295          |

## Limits of SINT used for conversions

| Constant                                       | type | Value  |
| ---------------------------------------------- | ---- | ------ |
| MIN_VALUE_OF_SINT_WHICH_CAN_BE_HELD_IN_A_BYTE  | SINT | SINT#0 |
| MIN_VALUE_OF_SINT_WHICH_CAN_BE_HELD_IN_A_WORD  | SINT | SINT#0 |
| MIN_VALUE_OF_SINT_WHICH_CAN_BE_HELD_IN_A_DWORD | SINT | SINT#0 |
| MIN_VALUE_OF_SINT_WHICH_CAN_BE_HELD_IN_A_LWORD | SINT | SINT#0 |
| MIN_VALUE_OF_SINT_WHICH_CAN_BE_HELD_IN_A_USINT | SINT | SINT#0 |
| MIN_VALUE_OF_SINT_WHICH_CAN_BE_HELD_IN_A_UINT  | SINT | SINT#0 |
| MIN_VALUE_OF_SINT_WHICH_CAN_BE_HELD_IN_A_UDINT | SINT | SINT#0 |
| MIN_VALUE_OF_SINT_WHICH_CAN_BE_HELD_IN_A_ULINT | SINT | SINT#0 |
| MIN_VALUE_OF_SINT_WHICH_CAN_BE_HELD_IN_A_TIME  | SINT | SINT#0 |
| MIN_VALUE_OF_SINT_WHICH_CAN_BE_HELD_IN_A_TOD   | SINT | SINT#0 |
| MIN_VALUE_OF_SINT_WHICH_CAN_BE_HELD_IN_A_DATE  | SINT | SINT#0 |
| MIN_VALUE_OF_SINT_WHICH_CAN_BE_HELD_IN_A_DT    | SINT | SINT#0 |

## Limits of INT used for conversions

| Constant                                      | type | Value    |
| --------------------------------------------- | ---- | -------- |
| MIN_VALUE_OF_INT_WHICH_CAN_BE_HELD_IN_A_BYTE  | INT  | INT#0    |
| MAX_VALUE_OF_INT_WHICH_CAN_BE_HELD_IN_A_BYTE  | INT  | INT#255  |
| MIN_VALUE_OF_INT_WHICH_CAN_BE_HELD_IN_A_WORD  | INT  | INT#0    |
| MIN_VALUE_OF_INT_WHICH_CAN_BE_HELD_IN_A_DWORD | INT  | INT#0    |
| MIN_VALUE_OF_INT_WHICH_CAN_BE_HELD_IN_A_LWORD | INT  | INT#0    |
| MIN_VALUE_OF_INT_WHICH_CAN_BE_HELD_IN_A_SINT  | INT  | INT#-128 |
| MAX_VALUE_OF_INT_WHICH_CAN_BE_HELD_IN_A_SINT  | INT  | INT#127  |
| MIN_VALUE_OF_INT_WHICH_CAN_BE_HELD_IN_A_USINT | INT  | INT#0    |
| MAX_VALUE_OF_INT_WHICH_CAN_BE_HELD_IN_A_USINT | INT  | INT#255  |
| MIN_VALUE_OF_INT_WHICH_CAN_BE_HELD_IN_A_UINT  | INT  | INT#0    |
| MIN_VALUE_OF_INT_WHICH_CAN_BE_HELD_IN_A_UDINT | INT  | INT#0    |
| MIN_VALUE_OF_INT_WHICH_CAN_BE_HELD_IN_A_ULINT | INT  | INT#0    |
| MIN_VALUE_OF_INT_WHICH_CAN_BE_HELD_IN_A_TIME  | INT  | INT#0    |
| MIN_VALUE_OF_INT_WHICH_CAN_BE_HELD_IN_A_TOD   | INT  | INT#0    |
| MIN_VALUE_OF_INT_WHICH_CAN_BE_HELD_IN_A_DATE  | INT  | INT#0    |
| MIN_VALUE_OF_INT_WHICH_CAN_BE_HELD_IN_A_DT    | INT  | INT#0    |

## Limits of DINT used for conversions

| Constant                                       | type | Value         |
| ---------------------------------------------- | ---- | ------------- |
| MIN_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_BYTE  | DINT | DINT#0        |
| MAX_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_BYTE  | DINT | DINT#255      |
| MIN_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_WORD  | DINT | DINT#0        |
| MAX_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_WORD  | DINT | DINT#65535    |
| MIN_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_DWORD | DINT | DINT#0        |
| MIN_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_LWORD | DINT | DINT#0        |
| MIN_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_SINT  | DINT | DINT#-128     |
| MAX_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_SINT  | DINT | DINT#127      |
| MIN_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_INT   | DINT | DINT#-32768   |
| MAX_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_INT   | DINT | DINT#32767    |
| MIN_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_USINT | DINT | DINT#0        |
| MAX_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_USINT | DINT | DINT#255      |
| MIN_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_UINT  | DINT | DINT#0        |
| MAX_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_UINT  | DINT | DINT#65535    |
| MIN_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_UDINT | DINT | DINT#0        |
| MIN_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_ULINT | DINT | DINT#0        |
| MIN_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_TIME  | DINT | DINT#0        |
| MIN_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_TOD   | DINT | DINT#0        |
| MAX_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_TOD   | DINT | DINT#86399999 |
| MIN_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_DATE  | DINT | DINT#0        |
| MIN_VALUE_OF_DINT_WHICH_CAN_BE_HELD_IN_A_DT    | DINT | DINT#0        |

## Limits of LINT used for conversions

| Constant                                       | type | Value            |
| ---------------------------------------------- | ---- | ---------------- |
| MIN_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_BYTE  | LINT | LINT#0           |
| MAX_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_BYTE  | LINT | LINT#255         |
| MIN_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_WORD  | LINT | LINT#0           |
| MAX_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_WORD  | LINT | LINT#65535       |
| MIN_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_DWORD | LINT | LINT#0           |
| MAX_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_DWORD | LINT | LINT#4294967295  |
| MIN_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_LWORD | LINT | LINT#0           |
| MIN_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_SINT  | LINT | LINT#-128        |
| MAX_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_SINT  | LINT | LINT#127         |
| MIN_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_INT   | LINT | LINT#-32768      |
| MAX_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_INT   | LINT | LINT#32767       |
| MIN_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_DINT  | LINT | LINT#-2147483648 |
| MAX_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_DINT  | LINT | LINT#2147483647  |
| MIN_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_USINT | LINT | LINT#0           |
| MAX_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_USINT | LINT | LINT#255         |
| MIN_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_UINT  | LINT | LINT#0           |
| MAX_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_UINT  | LINT | LINT#65535       |
| MIN_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_UDINT | LINT | LINT#0           |
| MAX_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_UDINT | LINT | LINT#4294967295  |
| MIN_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_ULINT | LINT | LINT#0           |
| MIN_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_TIME  | LINT | LINT#0           |
| MAX_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_TIME  | LINT | LINT#4294967295  |
| MIN_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_TOD   | LINT | LINT#0           |
| MAX_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_TOD   | LINT | LINT#86399999    |
| MIN_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_DATE  | LINT | LINT#0           |
| MAX_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_DATE  | LINT | LINT#4294944000  |
| MIN_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_DT    | LINT | LINT#0           |
| MAX_VALUE_OF_LINT_WHICH_CAN_BE_HELD_IN_A_DT    | LINT | LINT#4294967295  |

## Limits of USINT used for conversions

| Constant                                       | type  | Value     |
| ---------------------------------------------- | ----- | --------- |
| MAX_VALUE_OF_USINT_WHICH_CAN_BE_HELD_IN_A_SINT | USINT | USINT#127 |

## Limits of UINT used for conversions

| Constant                                       | type | Value      |
| ---------------------------------------------- | ---- | ---------- |
| MAX_VALUE_OF_UINT_WHICH_CAN_BE_HELD_IN_A_BYTE  | UINT | UINT#255   |
| MAX_VALUE_OF_UINT_WHICH_CAN_BE_HELD_IN_A_SINT  | UINT | UINT#127   |
| MAX_VALUE_OF_UINT_WHICH_CAN_BE_HELD_IN_A_INT   | UINT | UINT#32767 |
| MAX_VALUE_OF_UINT_WHICH_CAN_BE_HELD_IN_A_USINT | UINT | UINT#255   |

## Limits of UDINT used for conversions

| Constant                                        | type  | Value            |
| ----------------------------------------------- | ----- | ---------------- |
| MAX_VALUE_OF_UDINT_WHICH_CAN_BE_HELD_IN_A_BYTE  | UDINT | UDINT#255        |
| MAX_VALUE_OF_UDINT_WHICH_CAN_BE_HELD_IN_A_WORD  | UDINT | UDINT#65535      |
| MAX_VALUE_OF_UDINT_WHICH_CAN_BE_HELD_IN_A_SINT  | UDINT | UDINT#127        |
| MAX_VALUE_OF_UDINT_WHICH_CAN_BE_HELD_IN_A_INT   | UDINT | UDINT#32767      |
| MAX_VALUE_OF_UDINT_WHICH_CAN_BE_HELD_IN_A_DINT  | UDINT | UDINT#2147483647 |
| MAX_VALUE_OF_UDINT_WHICH_CAN_BE_HELD_IN_A_USINT | UDINT | UDINT#255        |
| MAX_VALUE_OF_UDINT_WHICH_CAN_BE_HELD_IN_A_UINT  | UDINT | UDINT#65535      |
| MAX_VALUE_OF_UDINT_WHICH_CAN_BE_HELD_IN_A_TOD   | UDINT | UDINT#86399999   |

## Limits of ULINT used for conversions

| Constant                                        | type  | Value                     |
| ----------------------------------------------- | ----- | ------------------------- |
| MAX_VALUE_OF_ULINT_WHICH_CAN_BE_HELD_IN_A_BYTE  | ULINT | ULINT#255                 |
| MAX_VALUE_OF_ULINT_WHICH_CAN_BE_HELD_IN_A_WORD  | ULINT | ULINT#65535               |
| MAX_VALUE_OF_ULINT_WHICH_CAN_BE_HELD_IN_A_DWORD | ULINT | ULINT#4294967295          |
| MAX_VALUE_OF_ULINT_WHICH_CAN_BE_HELD_IN_A_SINT  | ULINT | ULINT#127                 |
| MAX_VALUE_OF_ULINT_WHICH_CAN_BE_HELD_IN_A_INT   | ULINT | ULINT#32767               |
| MAX_VALUE_OF_ULINT_WHICH_CAN_BE_HELD_IN_A_DINT  | ULINT | ULINT#2147483647          |
| MAX_VALUE_OF_ULINT_WHICH_CAN_BE_HELD_IN_A_LINT  | ULINT | ULINT#9223372036854775807 |
| MAX_VALUE_OF_ULINT_WHICH_CAN_BE_HELD_IN_A_USINT | ULINT | ULINT#255                 |
| MAX_VALUE_OF_ULINT_WHICH_CAN_BE_HELD_IN_A_UINT  | ULINT | ULINT#65535               |
| MAX_VALUE_OF_ULINT_WHICH_CAN_BE_HELD_IN_A_UDINT | ULINT | ULINT#4294967295          |
| MAX_VALUE_OF_ULINT_WHICH_CAN_BE_HELD_IN_A_TIME  | ULINT | ULINT#4294967295          |
| MAX_VALUE_OF_ULINT_WHICH_CAN_BE_HELD_IN_A_TOD   | ULINT | ULINT#86399999            |
| MAX_VALUE_OF_ULINT_WHICH_CAN_BE_HELD_IN_A_DATE  | ULINT | ULINT#4294944000          |
| MAX_VALUE_OF_ULINT_WHICH_CAN_BE_HELD_IN_A_DT    | ULINT | ULINT#4294967295          |

## Limits of REAL used for conversions

| Constant                                       | type | Value                |
| ---------------------------------------------- | ---- | -------------------- |
| MIN_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_BYTE  | REAL | REAL#0               |
| MAX_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_BYTE  | REAL | REAL#255             |
| MIN_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_WORD  | REAL | REAL#0               |
| MAX_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_WORD  | REAL | REAL#65535           |
| MIN_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_DWORD | REAL | REAL#0               |
| MAX_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_DWORD | REAL | REAL#4.294967E+09    |
| MIN_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_LWORD | REAL | REAL#0               |
| MAX_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_LWORD | REAL | REAL#1.8446743E+19   |
| MIN_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_SINT  | REAL | REAL#-128            |
| MAX_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_SINT  | REAL | REAL#127             |
| MIN_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_INT   | REAL | REAL#-32768          |
| MAX_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_INT   | REAL | REAL#32767           |
| MIN_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_DINT  | REAL | REAL#-2.14748352E+09 |
| MAX_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_DINT  | REAL | REAL#2.14748352E+09  |
| MIN_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_LINT  | REAL | REAL#-9.223372E+18   |
| MAX_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_LINT  | REAL | REAL#9.223372E+18    |
| MIN_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_USINT | REAL | REAL#0               |
| MAX_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_USINT | REAL | REAL#255             |
| MIN_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_UINT  | REAL | REAL#0               |
| MAX_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_UINT  | REAL | REAL#65535           |
| MIN_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_UDINT | REAL | REAL#0               |
| MAX_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_UDINT | REAL | REAL#4.294967E+09    |
| MIN_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_ULINT | REAL | REAL#0               |
| MAX_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_ULINT | REAL | REAL#1.8446743E+19   |
| MIN_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_TIME  | REAL | REAL#0               |
| MAX_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_TIME  | REAL | REAL#4.294967E+09    |
| MIN_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_TOD   | REAL | REAL#0               |
| MAX_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_TOD   | REAL | REAL#8.639999E+07    |
| MIN_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_DATE  | REAL | REAL#0               |
| MAX_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_DATE  | REAL | REAL#4.294944E+09    |
| MIN_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_DT    | REAL | REAL#0               |
| MAX_VALUE_OF_REAL_WHICH_CAN_BE_HELD_IN_A_DT    | REAL | REAL#4.294967E+09    |

## Limits of LREAL used for conversions

| Constant                                         | type  | Value                         |
| ------------------------------------------------ | ----- | ----------------------------- |
| MIN_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_BYTE   | LREAL | LREAL#0                       |
| MAX_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_BYTE   | LREAL | LREAL#255                     |
| MIN_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_WORD   | LREAL | LREAL#0                       |
| MAX_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_WORD   | LREAL | LREAL#65535                   |
| MIN_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_DWORD  | LREAL | LREAL#0                       |
| MAX_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_DWORD  | LREAL | LREAL#4294967295              |
| MIN_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_LWORD  | LREAL | LREAL#0                       |
| MAX_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_LWORD  | LREAL | LREAL#1.844674407370955E+19   |
| MIN_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_SINT   | LREAL | LREAL#-128                    |
| MAX_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_SINT   | LREAL | LREAL#127                     |
| MIN_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_INT    | LREAL | LREAL#-32768                  |
| MAX_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_INT    | LREAL | LREAL#32767                   |
| MIN_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_DINT   | LREAL | LREAL#-2147483648             |
| MAX_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_DINT   | LREAL | LREAL#2147483647              |
| MIN_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_LINT   | LREAL | LREAL#-9.2233720368547758E+18 |
| MAX_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_LINT   | LREAL | LREAL#9.2233720368547758E+18  |
| MIN_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_USINT  | LREAL | LREAL#0                       |
| MAX_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_USINT  | LREAL | LREAL#255                     |
| MIN_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_UINT   | LREAL | LREAL#0                       |
| MAX_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_UINT   | LREAL | LREAL#65535                   |
| MIN_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_UDINT  | LREAL | LREAL#0                       |
| MAX_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_UDINT  | LREAL | LREAL#4294967295              |
| MIN_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_ULINT  | LREAL | LREAL#0                       |
| MAX_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_ULINT  | LREAL | LREAL#1.844674407370955E+19   |
| MIN_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_REAL   | LREAL | LREAL#-3.402823E+38           |
| MAX_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_REAL   | LREAL | LREAL#3.402823E+38            |
| MIN_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_TIME   | LREAL | LREAL#0                       |
| MAX_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_TIME   | LREAL | LREAL#4294967295              |
| MIN_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_TOD    | LREAL | LREAL#0                       |
| MAX_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_TOD    | LREAL | LREAL#86399999                |
| MIN_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_DATE   | LREAL | LREAL#0                       |
| MAX_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_DATE   | LREAL | LREAL#4294944000              |
| MIN_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_DT     | LREAL | LREAL#0                       |
| MAX_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_DT     | LREAL | LREAL#4294967295              |
| MAX_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_STRING | LREAL | LREAL#9.999999999999E+307     |
| MIN_VALUE_OF_LREAL_WHICH_CAN_BE_HELD_IN_A_STRING | LREAL | LREAL#-9.999999999999E+307    |

## Limits of TIME used for conversions

| Constant                                       | type | Value               |
| ---------------------------------------------- | ---- | ------------------- |
| MAX_VALUE_OF_TIME_WHICH_CAN_BE_HELD_IN_A_BYTE  | TIME | T#255MS             |
| MAX_VALUE_OF_TIME_WHICH_CAN_BE_HELD_IN_A_WORD  | TIME | T#1M5S535MS         |
| MAX_VALUE_OF_TIME_WHICH_CAN_BE_HELD_IN_A_SINT  | TIME | T#127MS             |
| MAX_VALUE_OF_TIME_WHICH_CAN_BE_HELD_IN_A_INT   | TIME | T#32S767MS          |
| MAX_VALUE_OF_TIME_WHICH_CAN_BE_HELD_IN_A_DINT  | TIME | T#24D20H31M23S647MS |
| MAX_VALUE_OF_TIME_WHICH_CAN_BE_HELD_IN_A_USINT | TIME | T#255MS             |
| MAX_VALUE_OF_TIME_WHICH_CAN_BE_HELD_IN_A_UINT  | TIME | T#1M5S535MS         |
| MAX_VALUE_OF_TIME_WHICH_CAN_BE_HELD_IN_A_TOD   | TIME | T#23H59M59S999MS    |

## Limits of TOD used for conversions

| Constant                                      | type | Value          |
| --------------------------------------------- | ---- | -------------- |
| MAX_VALUE_OF_TOD_WHICH_CAN_BE_HELD_IN_A_BYTE  | TOD  | TOD#0:0:0.255  |
| MAX_VALUE_OF_TOD_WHICH_CAN_BE_HELD_IN_A_WORD  | TOD  | TOD#0:1:5.535  |
| MAX_VALUE_OF_TOD_WHICH_CAN_BE_HELD_IN_A_SINT  | TOD  | TOD#0:0:0.127  |
| MAX_VALUE_OF_TOD_WHICH_CAN_BE_HELD_IN_A_INT   | TOD  | TOD#0:0:32.767 |
| MAX_VALUE_OF_TOD_WHICH_CAN_BE_HELD_IN_A_USINT | TOD  | TOD#0:0:0.255  |
| MAX_VALUE_OF_TOD_WHICH_CAN_BE_HELD_IN_A_UINT  | TOD  | TOD#0:1:5.535  |

## Limits of DATE used for conversions

| Constant                                       | type | Value       |
| ---------------------------------------------- | ---- | ----------- |
| MAX_VALUE_OF_DATE_WHICH_CAN_BE_HELD_IN_A_BYTE  | DATE | D#1970-1-1  |
| MAX_VALUE_OF_DATE_WHICH_CAN_BE_HELD_IN_A_WORD  | DATE | D#1970-1-1  |
| MAX_VALUE_OF_DATE_WHICH_CAN_BE_HELD_IN_A_SINT  | DATE | D#1970-1-1  |
| MAX_VALUE_OF_DATE_WHICH_CAN_BE_HELD_IN_A_INT   | DATE | D#1970-1-1  |
| MAX_VALUE_OF_DATE_WHICH_CAN_BE_HELD_IN_A_DINT  | DATE | D#2038-1-19 |
| MAX_VALUE_OF_DATE_WHICH_CAN_BE_HELD_IN_A_USINT | DATE | D#1970-1-1  |
| MAX_VALUE_OF_DATE_WHICH_CAN_BE_HELD_IN_A_UINT  | DATE | D#1970-1-1  |
| MAX_VALUE_OF_DATE_WHICH_CAN_BE_HELD_IN_A_TIME  | DATE | D#1970-2-19 |
| MAX_VALUE_OF_DATE_WHICH_CAN_BE_HELD_IN_A_TOD   | DATE | D#1970-1-1  |
| MAX_VALUE_OF_DATE_WHICH_CAN_BE_HELD_IN_A_DT    | DATE | D#2106-2-7  |

## Limits of DT used for conversions

| Constant                                     | type | Value                |
| -------------------------------------------- | ---- | -------------------- |
| MAX_VALUE_OF_DT_WHICH_CAN_BE_HELD_IN_A_BYTE  | DT   | DT#1970-1-1-0:4:15   |
| MAX_VALUE_OF_DT_WHICH_CAN_BE_HELD_IN_A_WORD  | DT   | DT#1970-1-1-18:12:15 |
| MAX_VALUE_OF_DT_WHICH_CAN_BE_HELD_IN_A_SINT  | DT   | DT#1970-1-1-0:2:7    |
| MAX_VALUE_OF_DT_WHICH_CAN_BE_HELD_IN_A_INT   | DT   | DT#1970-1-1-9:6:7    |
| MAX_VALUE_OF_DT_WHICH_CAN_BE_HELD_IN_A_DINT  | DT   | DT#2038-1-19-3:14:7  |
| MAX_VALUE_OF_DT_WHICH_CAN_BE_HELD_IN_A_USINT | DT   | DT#1970-1-1-0:4:15   |
| MAX_VALUE_OF_DT_WHICH_CAN_BE_HELD_IN_A_UINT  | DT   | DT#1970-1-1-18:12:15 |
| MAX_VALUE_OF_DT_WHICH_CAN_BE_HELD_IN_A_TIME  | DT   | DT#1970-2-19-17:2:47 |
| MAX_VALUE_OF_DT_WHICH_CAN_BE_HELD_IN_A_TOD   | DT   | DT#1970-1-1-23:59:59 |
