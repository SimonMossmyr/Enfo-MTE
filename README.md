# Enfo's Team Survival: MTExtended Edition

_Enfo's Team Survival: MTExtended Edition_ is a continuation of the abandoned WarCraft III map _Enfo's Team Survival: MT Edition_ by Pedro (Mecatronic) and Bruno (Prytoluk). It picks up where the developers left off at version 1.93 released in 2011.

## Instructions

### How to play in WarCraft III
Download the latest release in the [Releases](https://github.com/SimonMossmyr/Enfo-MTE/releases) tab and put the `.w3x` file in your WarCraft III maps folder: `X:\...\WarCraft III\Maps`. Start the game and play.

### How to open in World Editor
The `.w3x` under the [Releases](https://github.com/SimonMossmyr/Enfo-MTE/releases) tab is optimized and put under protection, so you can't open it in World Editor. To do this you require some third party software:

- WarCraft III 1.28,
- [SharpCraft WEX Bundle v0.1.3.0](https://www.hiveworkshop.com/threads/sharpcraft-world-editor-extended-bundle.292127/),
- [MPQ Recover v1.08](https://www.hiveworkshop.com/threads/mpq-recover-v1-08.249643/), 
- [MPQMaster v1.2.0](https://www.hiveworkshop.com/threads/mpq-master-v1-2-0.62935/).

Install said software and then proceed with these steps:

1. Clone this repo anywhere,
2. Make a copy of any `.w3x map` and place it anywhere. Some can be found in `X:\...\WarCraft III\Maps\FrozenThrone`,
3. Make a copy of `X:\...\Enfo-MTE-repository\mpq-listfile.txt` and place it in MPQMaster's listfile directory `X:\...\MPQ master v1.2.0\mpqmaster\Listfiles\`,
4. Open up said map in MPQMaster with the listfile and delete _all_ files in it,
5. Import all files and directories found in `X:\...\Enfo-MTE-repository\w3x-mpq-raw\` into the map,
6. Open the map using SharpCraft WEX.

Done. Make sure the map compiles and is playable using the Test Map button.

### How to commit changes to the map
After you've changed all you want in SharpCraft WEX, save the map, close it and follow these steps:

(Optional) If you have imported third party resources like custom button images, models or textures, you have to create a new MPQ listfile. Otherwise you can ignore steps:

1. Open up the map in MPQ Recover,
2. Tick the boxes for Brute Force and Deep Scan,
3. Scan the map,
4. Save two copies of the listfile: one in MPQMaster's listfile directory `X:\...\MPQ master v1.2.0\mpqmaster\Listfiles\` and one by overwriting this repository's existing listfile `X:\...\Enfo-MTE-repository\mpq-listfile.txt`

Then proceed as follows:

1. Open the map in MPQMaster using the listfile,
2. Extract _all_ files and directories found within to the repository's raw mpq folder `X:\...\Enfo-MTE-repository\w3x-mpq-raw\`,
3. Commit changes and create a Pull Request.

## Patch notes
Patch notes will (eventually) be found in the Wiki pages.

## FAQ
_Why have you made it so hard to open and edit the map in World Editor?_

> Version control and security. 
>
> Unfortunately, `.w3x` files are binary and any changes made in commits won't show up when using `$ git diff`. This means we can't be sure that any changes reported in the commit's message are actually the ones being made. Someone could potentially insert cheat codes without our knowledge, and this repository is public (or at least planned to be) so  anyone can make changes. 
>
> The solution is to extract all files in the map. All code in the map is in readable text files, and the other components (units, doodads, tileset, et.c.) are binary files which with some prying can actually be understood. This makes version control a lot easier.

_How did you crack the map?_

> Google it LOL.
