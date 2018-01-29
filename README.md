# Game Theory Cheat Sheet

**Game theory** is the study of mathematical models of conflict and cooperation between intelligent rational 
decision-makers.
Game theory is mainly used in economics, political science, and psychology, as well as logic, computer science and 
biology.

## Table of Content

- [Game Representations](#game-representations)
- [Classification of Games](#classification-of-games)

## Game Representations

**Players**: who are the decision makers?
- People? Governments? Companies? Somebody employed by a Company?...

**Actions**: what can the players do?
- Enter a bid in an auction? Decide whether to end a strike? Decide when to sell a stock? Decide how to vote?...

**Payoffs**: what motivates players?
- Do they care about some profit? Do they care about other players?...

#### Normal form

Lists what payoffs players get as a function of their actions. Usually represented by a matrix:

![Normal form](./assets/defining-games/normal-form.png)

#### Extensive form

Includes timing of moves. Usually represented by a tree.

![Extensive form](./assets/defining-games/extensive-form.png)

## Classification of Games

<table style="table-layout:fixed">
  <colgroup>
    <col style="width:50%"/>
    <col style="width:50%"/>
  </colgroup>
  <tr>
    <td>
      <p><b>Simultaneous game</b> (a.k.a. Strategy game) - a game where both players move simultaneously, or if they do
       not move simultaneously, the later players are unaware of the earlier players' actions (making them effectively
        simultaneous).
      <p>Usually normal form is used to represent simultaneous games.
    </td>
    <td>
      <p><b>Sequential game</b> (a.k.a. Extensive game) - a game where later players have some knowledge about earlier 
      actions.
      <p>Usually extensive form is used to represent sequential games.
    </td>
  </tr>
  <tr>
    <td>
      <b>Cooperative game</b> - a game where the players are able to form binding commitments externally enforced (e.g.
      through contract law).
    </td>
    <td>
      <b>Non-cooperative game</b> - a game where players cannot form alliances or if all agreements need to be
      self-enforcing (e.g. through credible threats).
    </td>
  </tr>
  <tr>
    <td>
      <b>Zero-sum game</b> - a game in which each participant's gain or loss of utility is exactly balanced by the
      losses or gains of the utility of the other participants.
    </td>
    <td>
      <b>Non-zero-sum game</b> - a game in which the interacting parties' aggregate gains and losses can be less
      than or more than zero.
    </td>
  </tr>
  <tr>
    <td>
      <b>Perfect information game</b> - a game in which all players know the moves previously made by all other players.
    </td>
    <td>
      <b>Imperfect information game</b> - a game in which some players don't know the moves previously made by other 
      players.
    </td>
  </tr>
  <tr>
    <td>
      <b>Complete information game</b> - a game in which all players know the strategies and payoffs available to the 
      other players.
    </td>
    <td>
      <b>Incomplete information game</b> - a game in which some players don't know the strategies or payoffs available
      to the other players.
    </td>
  </tr>
  <tr>
    <td>
      <b>Finite game</b> - a game that lasts for finite number of moves.
    </td>
    <td>
      <b>Infinite game</b> - a game that lasts for infinite number of moves.
    </td>
  </tr>
</table>

## Common Games

#### Prisoner's Dilemma

|                 | She stays silent  | She betrays     |
| --------------- | ----------------- | --------------- |
| He stays silent | -1,-1             | -3,0            |
| He betrays      | 0,-3              | **-2,-2**       |

- NE is to betray for both players. 
- This is a dominant strategies NE. 
- It is also the only non Pareto optimal outcome in this game.

#### Matching Pennies
 
|                  | She plays heads   | She plays tails  |
| ---------------- | ----------------- | ---------------- |
| He plays heads   | 1,-1              | -1,1             |
| He plays tails   | -1,1              | 1,-1             |
 
- It's a zero-sum game.
- There is a single NE in mixed strategies: each player chooses heads or tails with equal probability.

 #### Battle of the sexes
 
|                      | She goes to opera | She goes to football |
| -------------------- | ----------------- | -------------------- |
| He goes to opera     | 3,2               | 0,0                  |
| He goes to football  | 0,0               | 2,3                  |
 
- There are 3 NE:
  - Both players go to opera
  - Both players go to football
  - Mixed strategies NE: He goes to opera with probability 3/5, She goes to opera with probability 2/5.
