# Game Theory Cheat Sheet

**Game theory** is the study of mathematical models of conflict and cooperation between intelligent rational 
decision-makers.
Game theory is mainly used in economics, political science, and psychology, as well as logic, computer science and 
biology.

## Table of Content

- [Game Representations](#game-representations)
- [Classification of Games](#classification-of-games)
- [Commonly Known Games](#commonly-known-games)
- [Nash Equilibrium](#nash-equilibrium)
- [Extensive-Form Games](#extensive-form-games)
- [Repeated Games](#repeated-games)
- [Useful Links](#useful-links)

## Game Representations

**Players**: who are the decision makers?
- People? Governments? Companies? Somebody employed by a Company?...

**Actions**: what can the players do?
- Enter a bid in an auction? Decide whether to end a strike? Decide when to sell a stock? Decide how to vote?...

**Payoffs**: what motivates players?
- Do they care about some profit? Do they care about other players?...

#### Normal form

- Lists what payoffs players get as a function of their actions. 
- Does not incorporate any notion of sequence, or time, of the actions of the players.
- Usually represented by a matrix.

|                 | **Stay silent**       | **Betray**          |
| ---             | ---                   | ---                 |
| **Stay silent** | -1,-1                 | -3,0                |
| **Betray**      | 0,-3                  | **-2,-2**           |

#### Extensive form

- Includes timing of moves. 
- Usually represented by a tree.

![Extensive form](./assets/defining-games/extensive-form.png)

## Classification of Games

<table style="table-layout:fixed">
  <colgroup>
    <col style="width:50%"/>
    <col style="width:50%"/>
  </colgroup>
  <tr>
    <td>
      <p><b>Simultaneous games</b> (a.k.a. Strategy games) - games where both players move simultaneously, or if they do
       not move simultaneously, the later players are unaware of the earlier players' actions (making them effectively
        simultaneous).
      <p>Usually normal form is used to represent simultaneous games.
    </td>
    <td>
      <p><b>Sequential games</b> (a.k.a. Extensive game) - games where later players have some knowledge about earlier 
      actions.
      <p>Usually extensive form is used to represent sequential games.
    </td>
  </tr>
  <tr>
    <td>
      <b>Cooperative games</b> - games where the players are able to form binding commitments externally enforced (e.g.
      through contract law).
    </td>
    <td>
      <b>Non-cooperative games</b> - games where players cannot form alliances or if all agreements need to be
      self-enforcing (e.g. through credible threats).
    </td>
  </tr>
  <tr>
    <td>
      <b>Zero-sum games</b> - games in which each participant's gain or loss of utility is exactly balanced by the
      losses or gains of the utility of the other participants.
    </td>
    <td>
      <b>Non-zero-sum games</b> - games in which the interacting parties' aggregate gains and losses can be less
      than or more than zero.
    </td>
  </tr>
  <tr>
    <td>
      <b>Perfect information games</b> - games in which all players know the moves previously made by all other players.
    </td>
    <td>
      <b>Imperfect information games</b> - games in which some players don't know the moves previously made by other 
      players.
    </td>
  </tr>
  <tr>
    <td>
      <b>Complete information games</b> - games in which all players know the strategies and payoffs available to the 
      other players.
    </td>
    <td>
      <b>Incomplete information games</b> - games in which some players don't know the strategies or payoffs available
      to the other players.
    </td>
  </tr>
  <tr>
    <td>
      <b>Finite games</b> - games that last for finite number of moves.
    </td>
    <td>
      <b>Infinite games</b> - games that last for infinite number of moves.
    </td>
  </tr>
</table>

## [Commonly Known Games](https://en.wikipedia.org/wiki/List_of_games_in_game_theory)

#### [Prisoner's Dilemma](https://en.wikipedia.org/wiki/Prisoner%27s_dilemma)

|                 | **Stay silent**       | **Betray**          |
| ---             | ---                   | ---                 |
| **Stay silent** | -1,-1                 | -3,0                |
| **Betray**      | 0,-3                  | **-2,-2**           |

- There is 1 NE:
  - Both players betray. 
- This is a dominant strategies NE. 
- It is also the only non Pareto optimal outcome in this game.

#### [Matching Pennies](https://en.wikipedia.org/wiki/Matching_pennies)
 
|                      | **Play heads**      | **Play tails**     |
| ----                 | ---                 | ---                |
| **Play heads**       | 1,-1                | -1,1               |
| **Play tails**       | -1,1                | 1,-1               |
 
- There is 1 NE:
  - Mixed strategies NE: each player chooses heads or tails with probability 0.5.
- It's a zero-sum game.

#### [Battle of the Sexes](https://en.wikipedia.org/wiki/Battle_of_the_sexes_(game_theory))
 
|                          | **Go to opera**       | **Go to football**       |
| ---                      | ---                   | ---                      |
| **Go to opera**          | **3,2**               | 0,0                      |
| **Go to football**       | 0,0                   | **2,3**                  |
 
- There are 3 NE:
  - Both players go to opera
  - Both players go to football
  - Mixed strategies NE: He goes to opera with probability 3/5, She goes to opera with probability 2/5.
  
#### [Stag Hunt](https://en.wikipedia.org/wiki/Stag_hunt)
 
|                          | **Hunt stag**         | **Hunt hare**            |
| ---                      | ---                   | ---                      |
| **Hunt stag**            | **2,2**               | 0,1                      |
| **Hunt hare**            | 1,0                   | **1,1**                  |
 
- There are 3 NE:
  - Both players hunt stag
  - Both players hunt hare
  - Mixed strategies NE: He hunts stag with probability 2/3, She hunts stag with probability 2/3.

#### Free Money
 
|                      | **Play heads**      | **Play tails**     |
| ----                 | ---                 | ---                |
| **Play heads**       | **1,1**             | 0,0                |
| **Play tails**       | 0,0                 | **0,0**            |
 
- There are 2 NE (a rare case when there is an even number of NE):
  - Both players play heads
  - Both players play tails
  
#### [Chicken Game](https://en.wikipedia.org/wiki/Chicken_(game))
 
|                      | **Swerve**          | **Straight**        |
| ----                 | ---                 | ---                 |
| **Swerve**           | 0,0                 | **-1,1**            |
| **Straight**         | **1,-1**            | -10,-10             |
 
- Anti-coordination games - it is mutually beneficial for the players to play different strategies.
- There are 3 NE:
  - He swerves, she goes straight
  - He goes straight, she swerves
  - Mixed strategy NE: He swerves with probability 9/10, She swerves with probability 9/10
  
#### [Centipede Game](https://en.wikipedia.org/wiki/Centipede_game)

![Centipede Game](./assets/commonly-known-games/centipede-game.png)

- SPE: each player chooses to defect at every opportunity.
  
## Nash Equilibrium

**Nash Equilibrium** - a set of strategies, one for each player, such that no player has incentive to change
his strategy given what the other players are doing.

**Nash Equilibrium** (alternative definition) - a set of strategies, one for each player, such that every player's
strategy is the best response to what the other players are doing.

**Best Response** - a strategy such that a player cannot gain more utility from switching to a different strategy,
given what all other players are doing.

**Mixed Strategy** - a probability distribution over two or more pure strategies, that is, the players choose
randomly among their options in equilibrium. 

**Mixed Strategy Nash Equilibrium** - a set of mixed strategies, one for each player, such that no player has 
incentive to change his strategy given what the other players are doing.

**Dominant Strategy** - a strategy that is always better than any other strategy, for any profile of other players' 
actions.
  - Strictly Dominant Strategy - same as Dominant Strategy
  - Weakly Dominant Strategy - a strategy that is always better than or equal to any other strategy, for any profile of other players' actions.  

**Dominant Strategy Nash Equilibrium** - a Nash equilibrium in which all strategies are dominant. Can be found by
elimination of strictly dominated strategies.

**Dominated Strategy** - a strategy, such that, regardless of what any other players do, the strategy earns a player 
a smaller payoff than some other strategy. 
  - Strictly Dominated Strategy - same as Dominated Strategy
  - Weakly Dominated Strategy - a strategy, such that, regardless of what any other players do, the strategy earns a 
  player a smaller than or equal to some other strategy payoff.
  
**Pareto-optimal Outcome** - an outcome, such that there is no other outcome that Pareto-dominates it. An outcome `o` 
Pareto-dominates outcome `o'` if it's at least as good for every player as outcome `o'`, and there is some player
who strictly prefers `o` to `o'`.  

#### Nash's Theorem

Every finite, non-cooperative game of two or more players has a Mixed Strategy Nash Equilibrium. (John Nash, 1950)

#### The Oddness Theorem

Almost all finite games have a finite number of solutions, and that number is also odd. (Robert Wilson, 1971)

## Extensive-Form Games

#### Perfect Information Extensive-form Games

![Perfect Information Extensive-form Game](./assets/extensive-form-games/perfect-information-extensive-form-game.png)

All players know the moves previously made by all other players.

Every game in extensive form can be converted into normal form. The reverse transformation is not always possible, 
e.g. matching pennies cannot be written as a perfect information extensive form game.

#### Theorem

Every perfect information game in extensive form has a pure strategy Nash equilibrium.

#### Imperfect Information Extensive-form Games

![Imperfect Information Extensive-form Game](./assets/extensive-form-games/imperfect-information-extensive-form-game.png)

Player 2 doesn't know the move made by Player 1.

**Subgame Perfect Equilibrium** - Nash equilibrium that represents a Nash equilibrium of every subgame in the original 
game. It's a refinement of the Nash equilibrium that eliminates non-credible threats.

**Non-credible Threat** - a threat made by a player in an extensive form game which would not be 
in the best interest for the player to carry out. The hope is that the threat is believed in which case there is 
no need to carry it out. While Nash equilibria may depend on non-credible threats, Backward Induction eliminates them. 

## Repeated Games


## Incomplete Information Games

#### The Purification Theorem

Almost all mixed strategy Nash equilibria in a complete information game are the limit of pure strategy Bayesian Nash 
equilibria in an incomplete information game that converges to the complete information game.


## Useful Links

- Game Solver (2x2 matrix games): http://mindyourdecisions.com/GameSolver.html
