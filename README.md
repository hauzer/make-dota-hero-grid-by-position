![Demo](img/demo.gif)

## How To Install

If you're on Windows, you can download the latest [release](https://github.com/hauzer/dota-hero-grid-generator/releases). No guarantees it's the most up-to-date version, though.

If you want to run from source, follow these instructions:

* Ensure you have Python 3 installed.
*  `git clone git@github.com:hauzer/dota-hero-grid-generator.git`.
*  `cd dota-hero-grid-generator`.
*  `$PYTHON -m venv py`.
*  `py/Scripts/python -m pip install --upgrade git+https://github.com/anthony-tuininga/cx_Freeze.git@master`.
*  `py/Scripts/python -m pip install -r requirements.txt`.

## How To Use

* Point to the Steam installation directory in the `config.json` file.
* Set up your grids, also in the aforementioned file.
  * Multiple grids are supported, but you *can* have only one if you want.
  * Name the grids if you wish, using the `name` key. Otherwise, they'll be named automatically.
  * Set up your rank(s).
  * The `users` key denotes which Steam users use that particular grid. These usernames are account names (the thing you use to login), not nicknames. You need to set up that as well.
  * `pickrate_treshold` denotes the minimum percentage of matches a hero needs to be picked in a role for them to be included in that role. The default of 0.0336 indicates that the script will only include those heroes who would be picked at least twice in enough games to cover 119 pick choices for the respective role (which is two pick choices per game), that is at least once roughly every 30 games (in that role). Feel free to experiment.
  * Both of these are separated by roles (Core/Support).
* Run with `py/Scripts/python ./dota_hero_grid_generator.py`.

<sub>Data provided by [STRATZ](https://stratz.com).</sub>
