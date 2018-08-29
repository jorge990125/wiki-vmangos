Vanilla-MaNGOS is an open-source Vanilla WoW emulation project. It is a continuation of the Nost family of projects, which branched from MaNGOS-Zero several years ago. It was developed privately by the Nost team until late 2016, when the source code was transferred to the Elysium Project who made it open source. Unlike other emulation projects like cMaNGOS and TrinityCore which only seek to recreate the last patch of each expansion, this project aims to provide full content progression through Vanilla WoW.

## Useful Links

- [Server Repository](https://github.com/vmangos/core)
- [Database Repository](https://github.com/brotalnia/database)
- [Script Editor](https://github.com/brotalnia/scripteditor)

## What is what

The emulator has three major components. The first things you'll encounter are the binary files, the programs which make it possible to connect and play. Two there are, no more, no less. A login server (realmd) and a world server (mangosd). As its name implies, the login server handles player login, provides the list of available realms, and connects the client to the world server once he has successfully authenticated and chosen a realm. The world server is what makes the fun parts possible. It controls all in-game interactions and communicates with the player clients. It is what allows you to experience the world. It is the underlying laws of nature that govern how the world works. What the world contains is stored in the database. Without a database, the world would be empty, except for the naked players wandering around in the void. The database is the stuff you see in the world. It is the creatures you fight, the quests you go on, the items you struggle to acquire. The atoms the world is made of are defined in the database. All of this comes together to create the World of Warcraft that you play.

## Progression

What makes vMaNGOS special is that it aims to recreate all content changes throughout Vanilla WoW, starting all the way back from patch 1.2 to the 1.12 you are most familiar with. It is a project for the people who loved all of Vanilla and realize that 1.12 was only the end of the journey. In order to make this journey possible again, we've redesigned the way database data is stored and loaded. We've embraced the fact that things exist not only in space, but in time as well, so all content needs to have a value indicating when this particular version of it came into existence. These values start from 0 for patch 1.2, and go to 10 for patch 1.12. The world server will automatically load the most appropriate version of the content, based on the current patch value that is set in the configuration file. All it takes to change content patches is this one setting.