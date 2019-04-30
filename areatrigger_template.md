# The areatrigger_template table

Defines the location and size of all areatriggers.

## Structure

### 1. id - smallint(4) unsigned, primary key

An unique id.

### 2. build - tinyint(3) unsigned, primary key

Client build in which this exact version of the entry was added. The core will load the version of the entry with the highest build value that is not above the current supported build.

### 3. map_id - smallint(3) unsigned

Map id from the `map_template` table on which the trigger is located.

### 4. x - float

Global map coordinate of the exact center of the trigger.

### 5. y - float

Global map coordinate of the exact center of the trigger.

### 6. z - float

Global map coordinate of the exact center of the trigger.

### 7. radius - float

Size in yards of the trigger in all directions.

### 8. box_x - float

Specific size in yards of the trigger in the X axis. Most commonly used when radius is not specified.

### 9. box_y - float

Specific size in yards of the trigger in the Y axis. Most commonly used when radius is not specified.

### 10. box_z - float

Specific size in yards of the trigger in the Z axis. Most commonly used when radius is not specified.

### 11. box_orientation - float

Orientation of the trigger box. Most commonly used when radius is not specified.
