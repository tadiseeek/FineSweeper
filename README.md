# FineSweeper

Minimalistic functional Mine Sweeper (console, no mutable vars).

```plain
>
┏━┛┛┏━ ┏━┛┏━┛┃┃┃┏━┛┏━┛┏━┃┏━┛┏━┃
┏━┛┃┃ ┃┏━┛━━┃┃┃┃┏━┛┏━┛┏━┛┏━┛┏┏┛
┛  ┛┛ ┛━━┛━━┛━━┛━━┛━━┛┛  ━━┛┛ ┛
```

- [Interface](#interface)
    - [Command-line parameters](#command-line-parameters)
    - [In-Game Commands](#in-game-commands)

**System requirements:** Windows 10 x64, .NET Desktop Runtime 9.0.\
Linux and macOS are also supported with the corresponding .NET runtime.

ℹ️ For the best experience, use a modern UTF-8 terminal with emoji support, such as Windows Terminal (wt).

## Interface

### Command-line parameters

> finesweeper [width] [height] [mines] [seed]

#### Arguments

- width  - board width [3..26] default 12
- height - board height [3..26] default 12
- mines  - number of mines [3..99] default 10
- seed   - optional random seed (integer, optional)

ℹ️ The board will be the same for the same seed value.

#### Example runs

```shell
finesweeper
finesweeper 10 10 20
finesweeper 15 15 30 54321
finesweeper --help -h /? help
```

### In-Game Commands

- `r` X Y (r-Reveal) - Reveal the contents of the cell at column `X` and row `Y`.
    - `X` is a letter representing the horizontal coordinate (column).
    - `Y` is a number representing the vertical coordinate (row).
- `f` X Y (f-Flag) - Place or remove a flag on the cell at column `X` and row `Y` to mark a suspected mine.
- `q` (q-Quit) - Exit the game immediately.

For example:

```shell
|> r a 1
|> f e 3
|> q
```
