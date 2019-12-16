This table contains conditions that can be checked in scripts and other systems.

| Name            | Type                  | Comment                                              |
|-----------------|-----------------------|------------------------------------------------------|
| condition_entry | unsigned mediumint(8) | Primary key.                                         |
| type            | tinyint(3)            | The type of condition. See the types below.          |
| value1          | unsigned mediumint(8) | A value whose meaning depends on the condition type. |
| value2          | unsigned mediumint(8) | A value whose meaning depends on the condition type. |
| value3          | unsigned mediumint(8) | A value whose meaning depends on the condition type. |
| value4          | unsigned mediumint(8) | A value whose meaning depends on the condition type. |
| flags           | unsigned tinyint(3)   | 1 = reverse result 2 = swap targets                  |

A list of all conditions follows below.