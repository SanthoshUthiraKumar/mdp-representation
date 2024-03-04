# MDP REPRESENTATION

## AIM:
To represent a Markov Decision Process(MDP) problem in the following ways.
   1. Text representation
   2. Graphical representation
   3. Python - Dictonary representation

## PROBLEM STATEMENT:
To develop an environment in which a boy or a girl is going to school. The goal is to reach the school without getting lost.
### Problem Description
The agent has to reach the goal state(school) by taking the correct step towards the goal without drifting away from the path. After reaching the goal the agent will be rewarded if not then no reward will be provided.

### State Space
{0,1,2,3}

### Sample State
* 0 -> Starting point(S)
* 1 -> Relaxing point(R)
* 2 -> Goal point(G)
* 3 -> Restricted point(D)

### Action Space:
{1,2}

### Sample Action
{1} Moving up
{2} Moving down

### Reward Function

*  If the goal is reached -> reward=+1
*  Else -> reward=0

### Graphical Representation

![image](https://github.com/Evangelin-Ruth/mdp-representation/assets/94219798/0296a03e-f431-494a-8466-9817fc92fcb7)



## PYTHON REPRESENTATION:
```
School = { 
    #starting point state(S) ->0
    #Action: up-> 1, down-> 2
  0:{
     1:[(0.72 , 1 , 0,False),(0.28 , 0 , 0 , False)],
     2:[(0.82 , 0 , 0,False),(0.18 , 1 , 0 , False)] 
  },
    #Relaxing point state(R) ->1
  1:{
     1:[(0.98 , 2 , 0,False),(0.02 , 0 , 0 , False)],
     2:[(0.85 , 0 , 0,False),(0.15 , 2 , 0 , False)]
  },
    #Goal point state(G) ->2
  2:{
      1:[(0.82 , 3 , 1,True),(0.18 , 1 , 0 , False)],
      2:[(0.95 , 1 , 0,False),(0.05 , 3 , 1 , True)]
  },
    #Restricted point(R) ->3
  3:{
      1:[(0.92, 3 , 0, True),(0.08 , 2 , 0 , False)],
      2:[(0.88, 2 , 0, False),(0.12 , 3 , 0 , True)]
  }
}
School
```

## OUTPUT:

![image](https://github.com/Evangelin-Ruth/mdp-representation/assets/94219798/8449dbe0-1005-42da-b58f-075838983520)


## RESULT:
Thus a real world problem is represented as Markov Decision Problem in the following ways successfully:
 1. Text Representation
 2. Graphical Representation
 3. Python Representation
