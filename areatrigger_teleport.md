# The areatrigger_teleport table

Defines where areatriggers like dungeon portals teleport players, and the conditions to use them.

## Structure

### 1. id - mediumint(8) unsigned, primary key

Areatrigger id from the `areatrigger_template` table.

### 2. patch - tinyint(3) unsigned, primary key

Content patch in which this exact version of the entry was added. Patch values start from 0 for 1.2.4 and go up to 10 for 1.12.1. The core will load the version of the entry with the highest patch value that is not above the current patch.

### 3. name - text

The name of the location that this triggers teleports players to. This field is not used by the core.

### 4. required_level - tinyint(3) unsigned

Minimum level required to use the trigger.

### 5. required_item - mediumint(8) unsigned

Item id from the `item_template` table. This item will be required to use the trigger.

### 6. required_item2 - mediumint(8) unsigned

Item id from the `item_template` table. This item will be required to use the trigger.

### 7. required_quest_done - int(11) unsigned

Quest id from the `quest_template` table. Only players that have completed this quest can use the trigger.

### 8. required_event - int(11)

Game event id from the `game_event` table. If the value is positive, the event must be active to enter. If the value is negative, the event must be inactive to enter.

### 9. required_pvp_rank - mediumint(8) unsigned

Minimum honor rank to use the trigger. Used to restrict access to the Champions' Hall (Alliance) and Hall of Legends (Horde).

### 10. required_team - mediumint(8) unsigned

Player team faction that can use the trigger.
```
0 - Both
67 - Horde
469 - Alliance
```

### 11. target_map - smallint(5) unsigned

Map id from the `map_template` table where players will get teleported.

### 12. target_position_x - float

Global map coordinate of the location where players will get teleported.

### 13. target_position_y - float

Global map coordinate of the location where players will get teleported.

### 14. target_position_z - float

Global map coordinate of the location where players will get teleported.

### 15. target_orientation - float

The orientation that players will have once they get teleported.

