# Client Level Resource

## Level

A level is a playable object in Geometry Dash, namely coming with data that explains on what it is, and the string that the client interprets, known as a level string. It is stored in [XML](https://en.wikipedia.org/wiki/XML) format, and each level entry is a dictionary, containing key/value pairs denoting the level's properties.

### Level Data

**Level Structure**

| Key | Name/Value                     | Type                                                             | Description                                                                      |
| :-- | :----------------------------- | :--------------------------------------------------------------- | :------------------------------------------------------------------------------- |
| k1  | Level ID                       | **Integer**                                                      | the ID of the level                                                              |
| k2  | Level Name                     | **String**                                                       | the name of the level                                                            |
| k3  | Description                    | **String**                                                       | the level description, encoded in [base64](https://en.wikipedia.org/wiki/Base64) |
| k4  | Inner Level String             | **[Inner Level String](level-components/inner-level-string.md)** | the inner level string, or the playable level                                    |
| k5  | Creator                        | **[User](./user.md)Name**                                        | the name of the level creator                                                    |
| k6  | UserID                         | **Integer**                                                      | The UserID of the level Creator                                                  |
| k7  | Level Difficulty               | **Integer**                                                      | the difficulty the level has                                                     |
| k8  | Official Song ID               | **[Audio Track](/reference?id=audio-track)**                     | the official Song ID (if used)                                                   |
| k9  | Rating                         | **Integer**                                                      | The rating a level has                                                           |
| k10 | RatingSum                      | **Integer**                                                      | the sum of all the ratings a level has                                           |
| k11 | Downloads                      | **Integer**                                                      | the amount of times the level's been downloaded                                  |
| k12 | setCompletes                   | **Integer**                                                      | level completions for that particular level                                      |
| k13 | isEditable                     | **Boolean**                                                         | used to stop people editing online and Official levels                           |
| k14 | Verified                       | **Boolean**                                                         | whether the level is verified or not                                             |
| k15 | Uploaded                       | **Boolean**                                                         | whether the level is uploaded to the server or not                               |
| k16 | Level Version                  | **Integer**                                                      | the version of the level                                                         |
| k17 | Game Version                   | **Integer**                                                      | The Games Version                                                                |
| k18 | Attempts                       | **Integer**                                                      | the number of attempts that are made to this level                               |
| k19 | Normal Mode Percentage         | **Integer**                                                      | the max percentage that has been achieved in Normal Mods in this level           |
| k20 | Practice Mode Percentage       | **Integer**                                                      | the max percentage that has been achieved in Practice Mode in this level         |
| k21 | levelType                      | **Integer**                                                         | The Level Type (1 = Official, 2 = Local, 3 = Saved, 4 = Online)                  |
| k22 | Like Rating                    | **Integer**                                                      | the level's like rating (`likes - dislikes`)                                     |
| k23 | Length                         | **[Length](enumerations.md)**                                    | the level's length                                                               |
| k24 | Dislikes                       | **Integer**                                                      | how many dislikes a level has (unused)                                           |
| k25 | isDemon                        | **Boolean**                                                         | if the level is demon or not                                                     |
| k26 | Stars                          | **Integer**                                                      | the stars the level is worth                                                     |
| k27 | FeatureScore                   | **Integer**                                                      | A featured levels Feature Score                                                  |
| k33 | Auto                           | **Boolean**                                                         | If the level is auto                                                             |
| k34 | Replay Data                    | **[Gziped String](/topics/encryption/zip.md)**                   | Contains a Gzipped String which contains replay data for levels                  |
| k35 | isPlayable?                   | **Boolean**                                                        | if the level is downloaded (honestly not much is known about this)                                                           |
| k36 | Jumps                          | **Integer**                                                      | total Jumps on a level                                                           |
| k37 | required coins                 | **Integer**                                                      | coins required to unlock an official level                                       |
| k38 | isUnlocked                     | **Boolean**                                                         | is Official level Unlocked                                                       |
| k39 | level Size                     | **Integer**                                                      | `this->levelSize = std::floor(this->levelString.length() * 0.152);`              |
| k40 | Build Version                  | **Integer**                                                      | the games build version                                                          |
| k41 | Password                       | **Integer**                                                      | the [password]() <!-- local gamesave password topic link --> set for the level   |
| k42 | levelID                       | **Integer**                                                      | The ID of the level when its uploaded                                            |
| k43 | 2-Player Mode                | **Boolean**                                                         | If the level is 2 player mode                                                    |
| k45 | Custom Song ID                 | **Integer**                                                      | the custom Song ID (if used)                                                     |
| k46 | Level Revision                 | **Integer**                                                      | the revision of the level                                                        |
| k47 | hasBeenModified                | **Boolean**                                                         | if the level has been modified from outside the GD editor                        |
| k48 | Object Count                   | **Integer**                                                      | the object count of the level                                                |
| k50 | Binary Version                 | **Integer**                                                      | hardcoded to binary Version                                                      |
| k51 | capacity001                 | **Integer**                                                      | BatchNodes                                                     |
| k52 | capacity002                 | **Integer**                                                      | BatchNodes                                                    |
| k53 | capacity003                 | **Integer**                                                      | BatchNodes                                                     |
| k54 | capacity004                 | **Integer**                                                      | BatchNodes                                                      |
| k60 | AccountID                      | **Integer**                                                      | the Creators AccountID                                                           |
| k61 | First Coin Acquired            | **Boolean**                                                         | whether the first coin is acquired during verification                           |
| k62 | Second Coin Acquired           | **Boolean**                                                         | whether the second coin is acquired during verification                          |
| k63 | Third Coin Acquired            | **Boolean**                                                         | whether the third coin is acquired during verification                           |
| k64 | Total Coins                    | **Integer**                                                      | How many Coins the level has                                                     |
| k65 | areCoinsVerified                | **Boolean**                                                         | denotes if the coins are verified or not                                         |
| k66 | Requested Stars                | **Integer**                                                      | the requested stars during publication of the level                              |
| k67 | [Capacity String](/resources/client/level-components/capacity-string.md)                  | **String**                                                 | Contains batch information about levels                                          |
| k68 | triggeredAntiCheat             | **Boolean**                                                         | if you trigger the anticheat when beating demons                                 |
| k69 | High Object Count              | **Boolean**                                                         | If a level has a high object count                                               |
| k71 | Mana Orb Percentage          | **Integer**                                                      | the percentage up until the orb reward has been granted                          |
| k72 | hasLowDetailMode               | **Boolean**                                                         | If a level has LDM                                                               |
| k73 | toggleLDM                      | **Boolean**                                                         | If a LDM is Enabled                                                              |
| k74 | timelyID                       | **Integer**                                                      | the timelyID for a level                                                         |
| k75 | isEpic                         | **Boolean**                                                         | If a level has been awarded an epic rating                                       |
| k76 | demon type                     | **Integer**                                                      | Demon Type Enum                                                                  |
| k77 | isGauntlet                     | **Boolean**                                                         | Is the level in a gauntlet                                                       |
| k78 | isAltGame                      | **Boolean**                                                         | Levels that were completed on the free games                                     |
| k79 | Unlisted                       | **Boolean**                                                         | Whether the level is to be marked as unlisted or not during publication          |
| k80 | Seconds Spent Editing          | **Integer**                                                      | The number of seconds spent editing the level                                    |
| k81 | Seconds spent Editing (copies) | **Integer**                                                      | The number of seconds spent editing the level (Previous copies)                  |
| k82 | isLevelFavourited              | **Boolean**                                                         | If you put the level in your favourites                                          |
| k83 | levelOrder                     | **Integer**                                                      | Ordering for levels                                                              |
| k84 | Level Folder                   | **Integer**                                                      | The folder in which the level belongs (0 represents no folder)                   |
| k85 | Clicks                         | **Integer**                                                      | Clicks done on the best attempt                                                           |
| k86 | Player Time                    | **Integer**                                                      | The amount of time on a players best attempt           |
| k87 | level Seed                | **[LevelScoreSeed](/topics/encryption/chk?id=level-leaderboard)**| Contains info to verify the integrity of levelScores                             |
| k88 | Level Progress                 | **String**                                                      | Contains a list of high score differences seperated by a `,`                     |
| k89 | vfDChk | **Boolean**                    | Used to check for level completion                                               |
| k90 | Leaderboard percentage         | **integer**                                                      | Contains the percentage for level Leaderboards                      |


**Last Editor State Key/Value Pairs**
The last editor state key/value pairs contain a few values that indicate the last state of the editor before exiting the editor on that level.

| Key | Name/Value               | Type           | Description                              |
| :-- | :----------------------- | :------------- | :--------------------------------------- |
| kI1 | Editor Camera X Position | **Float**      | The X position of the editor camera      |
| kI2 | Editor Camera Y Position | **Float**      | The Y position of the editor camera      |
| kI3 | Editor Camera Zoom       | **Float**      | The zoom level of the editor camera      |
| kI4 | Build Tab Page           | **Integer**    | The displayed page within the build tab  |
| kI5 | Build Tab                | **Integer**    | The selected build tab                   |
| kI6 | Build Tab Pages          | **Dictionary** | The last browsed pages of each build tab |
| kI7 | Editor Layer             | **Float**      | The zoom level of the editor camera      |

Note that the build tab pages do not depend on the user's button row/column settings. That means, if the settings are changed, the build tab pages will not reflect the correct changes. For example:

The build tab page is 5, and the button settings are 6x2 (default), meaning the currently shown elements range from `5 * 6 * 2` = 60 to `6 * 6 * 2 - 1` = 71 (zero-indexed). If the user changes the button settings to 12x3, the tab page will remain as 5, showing elements ranging from `5 * 12 * 3` = 180 to `6 * 12 * 3 - 1` = 215 (zero-indexed).

### GDL22

<!-- from what i gathered, there doesnt seem to be any code that triggers these yet-->

**Current Unknown Values**

| Key | Type        | Info                                                     |
| :-- | :---------- | :------------------------------------------------------- |
| k91 | **String** | |
| k92 | **Integer** | |
| k93 | **Boolean** | Unlimited Objects? |
| k94 | **Boolean** | Platformer? |
