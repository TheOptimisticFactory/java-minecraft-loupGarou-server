# "Loup-Garou" micraft server

- This server is bundled with my public fork https://github.com/TheOptimisticFactory/LoupGarou/tree/dev which is based on the original repository https://github.com/leomelki/LoupGarou by `Leomelki` and `Shytoos`

- Placements provided in this repository are preconfigured for 12 participants using [this map](https://github.com/leomelki/LoupGarou/blob/master/maps/lg_village.zip). You should download the zip file and unzip it under `/world`

- The file `plugins/LoupGarou/config.yml` contains several important entries:
	+ `role` is the role distribution. It must match the number of players in your lobby before the game can start.
	+ `spawns` is the list of available spawn-points.
	+ `startingMemes` is the list of random sentences that will be picked at the begining of each game. You can customize them and/or add or remove entries to your liking.

### Useful commands (for ops) ###

- `/lg joinAll` to make everyone connected join the lobby
- `/lg start` to start the game
- `/lg end` to interrupt an ongoing game
- `/lg nick <username> <nickname>` to set a nickname to a player
- `/lg addSpawn` to add a spawn-point on your EXACT position and look direction
- `/lg roles` to get the list of currently active roles
- `/lg roles list` to get the complete list of available roles
- `/lg roles set <role> <amount>` to set the number of players for a given role