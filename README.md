# "Loup-Garou" server (Minecraft 1.15.2)

- This server is bundled with my public fork https://github.com/TheOptimisticFactory/LoupGarou/tree/dev which is based on the original repository https://github.com/leomelki/LoupGarou by `Leomelki` and `Shytoos`

## How to run the project ##

- Step n°01: Have Java installed
- Step n°02: Run the script `start.sh` in the terminal of your choice

- If you do not trust running this script directly just execute the following command in the main folder of this project: `java -DIReallyKnowWhatIAmDoingISwear -Xmx1024M -Xms1024M -jar spigot-1.15.2.jar nogui nogui`

## Configuration Tips ##

- Placements provided in this repository are pre-configured for 12 participants using [this map](https://github.com/leomelki/LoupGarou/blob/master/maps/lg_village.zip). You should download the zip file and unzip it under `/world`

- The file `plugins/LoupGarou/config.yml` contains several important entries:
	+ `role` is the role distribution. It must match the number of players in your lobby before the game can start.
	+ `spawns` is the list of available spawn-points.
	+ `startingMemes` is the list of random sentences that will be picked at the begining of each game. You can customize them and/or add or remove entries to your liking.

- The file `ops.json` is where you can configure which users will get admin permissions on your server

- The file `server.properties` is where you can configure every aspect of the minecraft server, such as max players, motd, etc.

## Useful commands (for ops) ##

- `/lg joinAll` to make everyone connected join the lobby
- `/lg start` to start the game
- `/lg end` to interrupt an ongoing game
- `/lg addSpawn` to add a spawn-point on your EXACT position and look direction
- `/lg roles` to get the list of currently active roles
- `/lg roles list` to get the complete list of available roles
- `/lg roles set <role> <amount>` to set the number of players for a given role

##### Additional commands compared to baseline repository:

- `/lg nick <username> <nickname>` to set a nickname to a player
- `/lg unnick <username>` to remove a nickname from a player
- `/lg random` to list the probability to picking each role with a weight > 0
- `/lg random showAll` to list the probability to picking each role (disregarding their weigth)
- `/lg random players <amount>` to set the number of players when using random role distribution

## Additional features compared to original plugin ##

As of today (2020/05/11), the original repository version is [v1.1.0](https://github.com/leomelki/LoupGarou/releases/tag/1.1.0), released on 2020/04/07.

My repository includes the **same content** along with the following **additions** (each link contains screenshots):

- [fork v1.2.0](https://github.com/TheOptimisticFactory/LoupGarou/releases/tag/v1.2.0) - Village composition showcase at the end of the game
- [fork v1.3.0](https://github.com/TheOptimisticFactory/LoupGarou/releases/tag/v1.3.0) - Ability to set nicknames to players + GUI to configure roles and start game
- [fork v1.4.0](https://github.com/TheOptimisticFactory/LoupGarou/releases/tag/v1.4.0) - Customizable memes messages at the start of the game + Highlight of the % of votes on a given player
- [fork v1.5.0](https://github.com/TheOptimisticFactory/LoupGarou/releases/tag/v1.5.0) - Revamped scoreboard to avoid useless scoring + Server logs when a player dies or gets resurrected
- [fork v1.6.0](https://github.com/TheOptimisticFactory/LoupGarou/releases/tag/v1.6.0) - Persisted round results for postgame analytics in CSV format
- [fork v1.7.0](https://github.com/TheOptimisticFactory/LoupGarou/releases/tag/v1.7.0) - Ability to hide the scoreboard to enable role bluffing
- [fork v1.8.0](https://github.com/TheOptimisticFactory/LoupGarou/releases/tag/v1.8.0) - Ability to randomize role attribution
- [fork v1.9.0](https://github.com/TheOptimisticFactory/LoupGarou/releases/tag/v1.9.0) - Revamped command parser + revamped codebase to ease adding new roles
- [fork v1.10.0](https://github.com/TheOptimisticFactory/LoupGarou/releases/tag/v1.10.0) - Added commands to showcase random distribution

## Additional features gallery ##

#### [fork v1.2.0] Village composition showcase at the end of the game

- https://github.com/leomelki/LoupGarou/pull/42 (Author: [TheOptimisticFactory](https://github.com/TheOptimisticFactory))

  ![image](https://user-images.githubusercontent.com/2607260/79672340-4260a780-81d1-11ea-9b49-266a992e872a.png)

#### [fork v1.3.0] Ability to set nicknames to players

- https://github.com/leomelki/LoupGarou/pull/40 (Author: [Nicooow](https://github.com/Nicooow)).
- Tweaked the PR with an [additional commit (9cbb739)](https://github.com/TheOptimisticFactory/LoupGarou/commit/9cbb73935532cacab8787cc4586a64e42b65958e) to:
  + support nickname containing spaces
  + color the nicknames

  ![image](https://user-images.githubusercontent.com/2607260/79674319-56f96b80-81e2-11ea-87ef-d4bdfd4494aa.png)

  ![javaw_Nk1NdY7KXw](https://user-images.githubusercontent.com/2607260/79673723-8e651980-81dc-11ea-8258-eb077bca7fca.png)

#### [fork v1.3.0] GUI to configure roles and start game

- https://github.com/leomelki/LoupGarou/pull/19 (Author: [Commantary](https://github.com/Commantary)).
- Tweaked the PR with an [additional commit (7df0439)](https://github.com/TheOptimisticFactory/LoupGarou/commit/7df04392ecb443d42207b859fcbbf4188e8080ae) to:
  + fix compilation issues

  ![image](https://user-images.githubusercontent.com/2607260/80097236-41ca6700-856b-11ea-978c-dd658ad09c67.png)

#### [fork v1.4.0] Highlight of the % of votes on a given player

- https://github.com/leomelki/LoupGarou/pull/43 (Author: [TheOptimisticFactory](https://github.com/TheOptimisticFactory))

  ![image](https://user-images.githubusercontent.com/2607260/79676799-f706c300-81e9-11ea-86cd-0c9cd98be0b3.png)

#### [fork v1.5.0] Server logs when a player dies or gets resurrected

- https://github.com/leomelki/LoupGarou/pull/47 (Author: [TheOptimisticFactory](https://github.com/TheOptimisticFactory))

  ![image](https://user-images.githubusercontent.com/2607260/80264401-56564e80-8694-11ea-9f28-89a425b4d59b.png)

#### [fork v1.5.0] Revamped scoreboard to avoid useless scoring

- Needs testing before the PR gets created. (Author: [TheOptimisticFactory](https://github.com/TheOptimisticFactory))
  + Added highlight of the total number of players remaining.
  + Added support of plural names in the scoreboard.
  + Rewritten logic to avoid instantiating 15 instances when 1 is sufficient.

  ![javaw_3n08F7Wy4V](https://user-images.githubusercontent.com/2607260/80318956-faafd080-880d-11ea-8a82-5d7a63f66330.png)

#### [fork v1.6.0] Persisted round results for postgame analytics

- Needs testing before the PR gets created. (Author: [TheOptimisticFactory](https://github.com/TheOptimisticFactory))
- Village composition and victory type is saved in `stats.csv` to enable postgame analytics

  ![Code_FCvEXfwuZR](https://user-images.githubusercontent.com/2607260/80318997-54b09600-880e-11ea-9256-a29da3f42175.png)

#### [fork v1.8.0] Ability to randomize role attribution

- Needs testing before the PR gets created. (Author: [TheOptimisticFactory](https://github.com/TheOptimisticFactory))
- The roles can now be randomly distributed using a weighting system to set the likelihood of each individual role. The higher the weight, the more likely it will be picked compared to others. See [release v1.8.0](https://github.com/TheOptimisticFactory/LoupGarou/releases/tag/v1.8.0) for how it works

  ![image](https://user-images.githubusercontent.com/2607260/82044533-cc573f80-96ad-11ea-8511-04de99d4fd75.png)
