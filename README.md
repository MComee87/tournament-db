# tournament-db

This repository uses virtualbox, vagrant and postgresql to manage a Swiss tournament style tracking.

## Installation

Clone this repository using:

`git clone https://github.com/MComee87/tournament-db`


## Usage

1. First change into the tournament directory:

	`~/tournament-db/vagrant/tournament`

2. Second create the database by starting up postgresql and executing the following command:

	`CREATE DATABASE tournament;`

3. Set up the tables in the database in postgresql by executing the following command:

	`\i tournament.sql`

4. Exit postgresql, then test the program using:

	`python tournament_test.py`

5. The test program should verify that the below functions are working properly.

	* deleteMatches()
		- Clear all scores from a tournament to restart the tournament with the same players.

	* deletePlayers()
		- Clear the tournament to start with new players.

	* registerPlayer(player_name)
		- Register a player in the tournament.

	* countPlayers()
		- Count the number of players in the tournament.

	* playerStandings()
		- Get the player standings.

	* reportMatch(id_of_winner, id_of_loser)
		- Update the tournament results by reporting the winner and loser of a match.

	* swissPairings()
		- Get the pairings for the next matches.
