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
- [Bayesian Games](#bayesian-games)
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

**Positive affine transformation**: au + b, where a > 0
and b is any real number. Expected utilities are identical to positive affine transformations. 

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

#### [Coordination Games](https://en.wikipedia.org/wiki/Coordination_game)

- [Battle of the Sexes](#battle-of-the-sexes)
- [Stag Hunt](#stag-hunt)
- [Pure Coordination Game](#pure-coordination-game)

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

#### Pure Coordination Game
 
|                          | **Go to Party**       | **Stay Home**            |
| ---                      | ---                   | ---                      |
| **Go to Party**          | **10,10**             | 0,0                      |
| **Stay Home**            | 0,0                   | **5,5**                  |
 
- There are 3 NE:
  - Both players go to party
  - Both players stay home
  - Mixed strategies NE: He goes to party with probability 1/3, She goes to party with probability 1/3.

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
 
[Subgame Perfect Equilibrium](#extensive-form-games)

[Bayesian Nash Equilibrium](#bayesian-games)

Nash equilibrium depending on the type of game:
 
|                     | **Simultaneous**       | **Sequential**          |
| ---                 | ---                    | ---                     |
| **Complete**        | Nash                   | Subgame Perfect Nash    |
| **Incomplete**      | Bayesian Nash          | Perfect Bayesian Nash   |
  
**Pareto-optimal Outcome** - an outcome, such that there is no other outcome that Pareto-dominates it. An outcome `o` 
Pareto-dominates outcome `o'` if it's at least as good for every player as outcome `o'`, and there is some player
who strictly prefers `o` to `o'`.  

#### Nash's Theorem

Every finite, non-cooperative game of two or more players has a mixed strategy Nash equilibrium. (John Nash, 1950)

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

**Backward Induction** - identify the equilibria in the bottom-most trees, and adopt these as one moves up the tree.

**Subgame Perfect Equilibrium** - Nash equilibrium that represents a Nash equilibrium of every subgame in the original 
game. It's a refinement of the Nash equilibrium that eliminates non-credible threats.

**Non-credible Threat** - a threat made by a player in an extensive form game which would not be 
in the best interest for the player to carry out. The hope is that the threat is believed in which case there is 
no need to carry it out. While Nash equilibria may depend on non-credible threats, Backward Induction eliminates them. 

## Repeated Games

**Repeated Game** - an extensive form game that consists of a number of repetitions of some base game, called 
a stage game. The stage game is usually one of the well-studied 2-person games.

**Discount Factor** - a number between 0 and 1 that represents the time value of consumption and probability of 
continuation. A higher discount factor means more patience and higher chance of surviving into the next period.

**The One-Shot Deviation Principle** - in finite or infinitely repeated games with discounting, a set of strategies 
is a subgame perfect equilibrium iff no player can profitably deviate from his strategy at a single stage and maintain 
his strategy everywhere else.

**Grim Trigger** - play some set of strategies with higher payoff than NE, if anyone deviates then play NE forever.

**Tit-for-Tat** - a strategy in the infinitely repeated prisoner's dilemma:
  - Begin by cooperating
  - For all future periods, copy opponent's strategy from the previous period.

Both players playing tit-for-tat is not subgame perfect.
  
**Stochastic Game** - a generalization of repeated games.
  - agents repeatedly play games from a set of normal-form games.
  - the game played at any iteration depends on the previous game played and on the actions taken by all agents in 
  that game.

#### The Folk theorem 
  - Take a Nash equilibrium from the stage game
  - Consider any alternative set of strategies such that the expected utility for those strategies in the stage game is 
  strictly greater for all players
  - If discounting factor is sufficiently high, a subgame perfect equilibrium exists in which players use those 
  alternative strategies on the equilibrium path.
  
Implications of the folk theorem:
  - If the purpose of equilibrium is to predict or explain outcomes, subgame perfect equilibrium predicts and explains
  everything
  - Predicting and explaining everything is essentially predicting and explaining nothing
  
#### Learning in Repeated Games:
**Fictitious Play**: each player maintains explicit belief about the other players.
  - Initialize beliefs about the opponent's strategies.
  - Each turn: 
    - Play best response to the assessed strategy of the opponent
    - Observe the opponent's actual play and update beliefs accordingly.

**No-regret Learning**:  

## Bayesian Games

**Bayesian Game** - a set of games that differ only in their payoffs, a common prior defined over them, and a 
partition structure over the games for each agent.

Bayesian game is a representation of a game with incomplete information.

**Bayesian Nash Equilibrium** - a set of strategies, one for each type of player, such that no type has incentive to change his or her strategy given the beliefs about the types and what the  other types are doing.

**Ex Ante Dominated Strategy** - a strategy for a player such that an alternative strategy for that player provides a greater payoff for that player regardless of all other players' strategies

**Interim Dominated Strategy** - a strategy for a type such that an alternative strategy for that type provides a greater payoff for that type regardless of all other players' strategies

Interim dominated strategy implies ex ante dominated strategies. The reverse is not always true.

#### The Purification Theorem

Almost all mixed strategy Nash equilibria in a complete information game are the limit of pure strategy Bayesian Nash 
equilibria in an incomplete information game that converges to the complete information game.


## Useful Links

- Game Solver (2x2 matrix games): http://mindyourdecisions.com/GameSolver.html
