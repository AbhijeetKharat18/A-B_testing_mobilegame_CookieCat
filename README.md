# A-B_testing_mobilegame_CookieCat
A/B testing: Analyzing the Impact of Relocating the First Gate in Cookie Cats on Player Retention.

Cookie Cats is a mobile puzzle game that requires players to connect tiles of the same colour to win the level. 
To increase player enjoyment and prolong game-play, gates are placed at certain levels to force players to take a break or make an in-app purchase. 
This project analyses an A/B-test that moved the first gate from level 30 to level 40, and looks at the impact on player retention.








The A/B-test data
The data we have is from 90,189 players that installed the game while the AB-test was running. 

The variables are:
  userid - a unique number that identifies each player.
  version - whether the player was put in the control group (gate_30 - a gate at level 30) or the group with the moved gate (gate_40 - a gate at level 40).
  sum_gamerounds - the number of game rounds played by the player during the first 14 days after install.
  retention_1 - did the player come back and play 1 day after installing?
  retention_7 - did the player come back and play 7 days after installing?

Steps followed-

a.When a player installed the game, he or she was randomly assigned to either gate_30 or gate_40.
  Performed sanity check for verification of distribution.


b.Overall 1-day retention.

  A common metric in the video gaming industry for how fun and engaging a game is 1-day retention: 
  The percentage of players that comes back and plays the game one day after they have installed it. 
  The higher 1-day retention is, the easier it is to retain players and build a large player base.
  
  
c.1-day retention by AB-group.

  A-group: gate_30
  B-group: gate_40
  
  
  
d.Should we be confident in the difference?

  while we are certain of the difference in the data, how certain should we be that a gate at level 40 will be worse/better in the future?
  Bootstrapping can be used to determine the certainty of the 1-day retention numbers. 
  The process involves repeatedly re-sampling the dataset (with replacement) and calculating 1-day retention for each sample. 
  The variation in 1-day retention will provide an indication of the uncertainty of the numbers.
  
  
  
e.Zooming in on the difference

  Performed validation by plotting of the bootstrap difference graph
  
  
  
f.7-day retention by AB-group

  The bootstrap analysis suggests that 1-day retention is higher when the gate is set at level 30. 
  However, since most players have not yet reached level 30, it is important to also consider 7-day retention when considering the effects of the gate. 
  7-day retention measures the percentage of players who return to the game a week after installing it.
  
  
g.Zooming in on the difference

  Performed validation by plotting of the bootstrap difference graph
  
  
h.Conclusion

  Should we move the gate from level 30 to level 40 ? = Nope
  
