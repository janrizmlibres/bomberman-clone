# Bomberman: Re

A two-player Bomberman clone in Java, built with libGDX and Box2D. Two players share one keyboard on a single arena, dropping bombs to break blocks, collect power-ups and blow each other up.

## How a match plays

- Each round runs on a 300 second clock. A round ends when a player dies or the clock runs out, and the arena resets for the next one.
- The first player to win 3 rounds wins the match.
- Breakable blocks can drop one of three power-ups: more bomb range, more bombs at once, or more speed.
- In the last 60 seconds of a round both players jump to maximum stats.

## Controls

| | Move | Bomb |
|---|---|---|
| Player 1 | `W` `A` `S` `D` | `F` |
| Player 2 | Arrow keys | `Enter` |

## Running it

You need a JDK. The Gradle wrapper (Gradle 7.5.1) pulls in libGDX 1.11.0, so there is nothing else to install.

```
git clone https://github.com/janrizmlibres/bomberman-clone.git
cd bomberman-clone
./gradlew desktop:run
```

On Windows use `gradlew.bat desktop:run`. The run task adds `-XstartOnFirstThread` on macOS for you.

## Project layout

- `core/` holds the game code, split into packages for actors, objects, effects and screens.
- `desktop/` holds the LWJGL3 launcher.
- `assets/` holds the sprites and audio, plus the Tiled map in `tilemaps/level1.tmx`.

## Status

Finished and no longer worked on. The font is loaded from a Windows-style path (`sprites\bm.ttf`), so it may fail to load on macOS and Linux until that is changed to a forward slash. The Box2D debug renderer is still drawn over the map.

## License

MIT. See [LICENSE](LICENSE).
