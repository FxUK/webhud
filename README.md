![R3E](https://cloud.githubusercontent.com/assets/12783101/8024034/cd3c7c84-0d24-11e5-9e5f-3bf6fbab713f.png)

---

![Preview](https://raw.githubusercontent.com/sector3studios/webhud/master/src/img/preview.jpg)

# Web Hud

This is a sample showing how to create a web hud using the shared memory API for
[RaceRoom Racing Experience][r3e] (R3E).

For discussions or support go [here](https://forum.sector3studios.com/index.php?threads/in-gameplay-web-overlays.12947/).

## Quick start

-   Extract [public/dash.zip](public/dash.zip)
-   Run dash.exe
-   Add `-webHudUrl=https://fxuk.github.io/webhud/dist/` to the game launch arguments
-   Start the game

## CHANGES TO ORIGINAL BRANCH IN DIST

My current changes include:
Transparent Radar, with dark background and border removed.
Radar shows more prominently when in proximity to another car.

Relative hud shows relative time to cars ahead / behind, rather than distance.
This is not relative time to 'leaderboard position' but to the actual vehicle
Background colour of rows on relative hud change to blue/red depending if you are lapping or being lapped by the car infront/behind.


## Development

-   Development requires node/npm
-   For this to work you need to be running `public/dash.zip/dash.exe`. It is the source of all the data being used.
-   Start development by running `npm start` and opening http://localhost:4000/
-   Add `-webdev -webHudUrl=http://localhost:4000/` to the game launch arguments
-   When you are happy with your changes run `npm run build` and the final files will be put in the `dist/` folder.

## Tips

-   Look at `src/types/r3eTypes.ts` to see what data is exposed
-   Press `Shift+i` to view the current game state (search takes regex)
-   Press `Shift+Space` to freeze the current game state
-   Press `Shift+d` to dump current game state as JSON into clipboard
-   Press `Ctrl+v` to insert dumped JSON game state into current session

## License

See [LICENSE](LICENSE).

[r3e]: http://game.raceroom.com/
