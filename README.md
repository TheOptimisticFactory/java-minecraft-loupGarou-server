# "Loup-Garou" server (Minecraft 1.15.2)

- This server is bundled with my public fork https://github.com/TheOptimisticFactory/LoupGarou/tree/dev which is based on the original repository https://github.com/leomelki/LoupGarou by `Leomelki` and `Shytoos`

- Placements provided in this repository are preconfigured for 12 participants using [this map](https://github.com/leomelki/LoupGarou/blob/master/maps/lg_village.zip). You should download the zip file and unzip it under `/world`

- The file `plugins/LoupGarou/config.yml` contains several important entries:
	+ `role` is the role distribution. It must match the number of players in your lobby before the game can start.
	+ `spawns` is the list of available spawn-points.
	+ `startingMemes` is the list of random sentences that will be picked at the begining of each game. You can customize them and/or add or remove entries to your liking.

## Useful commands (for ops) ##

- `/lg joinAll` to make everyone connected join the lobby
- `/lg start` to start the game
- `/lg end` to interrupt an ongoing game
- `/lg nick <username> <nickname>` to set a nickname to a player
- `/lg addSpawn` to add a spawn-point on your EXACT position and look direction
- `/lg roles` to get the list of currently active roles
- `/lg roles list` to get the complete list of available roles
- `/lg roles set <role> <amount>` to set the number of players for a given role

## Notes ##

- The following warning is normal and can safely be ignored: `WARNING: Illegal reflective access by com.comphenix.net.sf.cglib.core.ReflectUtils$1 (file:<path>) to method java.lang.ClassLoader.defineClass(java.lang.String,byte[],int,int,java.security.ProtectionDomain)`. It is due to the fact that [ProtocolLib currently does not support Java versions above Java 8 and won't until Mojang and Spigot decide to update.](https://github.com/dmulloy2/ProtocolLib/issues/603#issuecomment-490207994)

## Additional features compared to original plugin ##

#### 01) Village composition showcase at the end of the game

- https://github.com/leomelki/LoupGarou/pull/42 (Author: [TheOptimisticFactory](https://github.com/TheOptimisticFactory))

  ![image](https://user-images.githubusercontent.com/2607260/79672340-4260a780-81d1-11ea-9b49-266a992e872a.png)

#### 02) Ability to set nickanmes to players

- https://github.com/leomelki/LoupGarou/pull/40 (Author: [Nicooow](https://github.com/Nicooow)).
- Tweaked the PR with an [additional commit (9cbb739)](https://github.com/TheOptimisticFactory/LoupGarou/commit/9cbb73935532cacab8787cc4586a64e42b65958e) to:
  + support nickname containing spaces
  + color the nicknames

  ![image](https://user-images.githubusercontent.com/2607260/79674319-56f96b80-81e2-11ea-87ef-d4bdfd4494aa.png)

  ![javaw_Nk1NdY7KXw](https://user-images.githubusercontent.com/2607260/79673723-8e651980-81dc-11ea-8258-eb077bca7fca.png)

#### 03) GUI to configure roles and start game

- https://github.com/leomelki/LoupGarou/pull/19 (Author: [Commantary](https://github.com/Commantary)).
- Tweaked the PR with an [additional commit (7df0439)](https://github.com/TheOptimisticFactory/LoupGarou/commit/7df04392ecb443d42207b859fcbbf4188e8080ae) to:
  + fix compilation issues

  ![image](https://user-images.githubusercontent.com/2607260/80097236-41ca6700-856b-11ea-978c-dd658ad09c67.png)

#### 04) Highlight of the % of votes on a given player

- https://github.com/leomelki/LoupGarou/pull/43 (Author: [TheOptimisticFactory](https://github.com/TheOptimisticFactory))

  ![image](https://user-images.githubusercontent.com/2607260/79676799-f706c300-81e9-11ea-86cd-0c9cd98be0b3.png)

#### 05) Server logs when a player dies or gets resurrected

- https://github.com/leomelki/LoupGarou/pull/47 (Author: [TheOptimisticFactory](https://github.com/TheOptimisticFactory))

  ![image](https://user-images.githubusercontent.com/2607260/80264401-56564e80-8694-11ea-9f28-89a425b4d59b.png)

#### 06) Revamped scoreboard to avoid useless scoring

- Needs testing before the PR gets created. (Author: [TheOptimisticFactory](https://github.com/TheOptimisticFactory))
  + Added highlight of the total number of players remaining.
  + Added support of plural names in the scoreboard.
  + Rewritten logic to avoid instantiating 15 instances when 1 is sufficient.

  ![javaw_3n08F7Wy4V](https://user-images.githubusercontent.com/2607260/80318956-faafd080-880d-11ea-8a82-5d7a63f66330.png)

#### 07) Persisted round results for postgame analytics

- Needs testing before the PR gets created. (Author: [TheOptimisticFactory](https://github.com/TheOptimisticFactory))
- Village composition and victory type is saved in `stats.csv` to enable postgame analytics

  ![Code_FCvEXfwuZR](https://user-images.githubusercontent.com/2607260/80318997-54b09600-880e-11ea-9256-a29da3f42175.png)

