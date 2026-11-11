# dorfromantik_helper
A basic GUI helper tool for Dorfromantik

### Installation instructions (windows)

* Download the code from the github repository and extract it

* Open Command Prompt

* Navigate to the downloaded code (ex. `cd path\to\my\folder\dorfromantik-helper`)

* Install python by running the command `python`, which should open the app store

* Run `pip install -r requirements.txt` to install the required packages

Setup is complete. Run `python app.py` to run the program

### Usage
`python app.py --help` provides information on available command line arguments

Example usage:
`python app.py --width 1000 --height 600 --layout 0`

To load a saved board, add the `--load` argument

### Changes in this fork
Four changes on top of the original (which hasn't been updated since 2021):

- Each hinted placement shows its score as a number on the tile.
- The score weighs perfect and ruined tiles more heavily: +3 per perfect tile, +1 per good connection, -2 per bad connection and -5 per ruined neighbor (the original used +0.5, +1, -0.5 and -1).
- The hint list shows up to 50 placements with a score of 0 or more, instead of 10 with a score of 2 or more (if fewer than 5 qualify, it shows the best 5 regardless of score).
- Fixed hints not appearing when every possible placement scored above the cutoff, or when there was no legal placement at all.
