## General idea:
Get all the platforms location.
Consider each platform as a node, and the goal is to construct an adjacency graph based on it, where the weight is the time required to get from one to another.

## How to determine if two nodes are connected?
To check if two nodes are connected, we have two criterias:
- if it passes the __walk__ test
- if it passes the __jump__ test
satisfying either one of them means they are connected (in fact, satisfying __walk__ test <i>guarantees</i> to satisfy the __jump__ test)

## walk test
if two nodes share the same vertical coordinate, and a consecutive horizontal coordinate (e.g.)