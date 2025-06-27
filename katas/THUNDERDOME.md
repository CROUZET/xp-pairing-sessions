# ⚔️ THUNDERDOME ⚔️

Welcome to another edition of..........  THUNDERDOME!!!!!!!!!

> "Two Men Enter, One Man Leaves"

## Goal

Given 2 fighters, tell the one who will leave the thunderdome alive

Fighters have characteristics:
- ATTACK -> how much damage an attack reduce the opponent HP
- DEFENSE -> how much damage are reduced from an opponent's attack
- STAMINA -> durability of the DEFENSE and effectiveness of the ATTACK
- HP -> the quantity of HP
- SPEED -> how fast the fighter begins the fight

Each in turn, a fighter perform an attack to the opponent. 

The function must have 2 fighters in input and return the name of the winner

## Specs

The fighter with the more SPEED starts first.

An attack damage follows the formula: ATTACK - (opponent's DEFENSE)

When a fighter attack: 
 - his STAMINA is reduced by 1/2 of the ATTACK (rounded)
 - the opponent's STAMLINA is reduced by 1/4 of the ATTACK (rounded)

When a fighter reaches zero STAMINA :
- his DEFENSE is zero
- his ATTACK is halved

When a fighter reaches zero HP, he dies

Every attributes must be at least 1

## Options
- 
- DEFENSE management can be ignored for a start
- STAMINA management can be ignored for a start
- More than 2 fighters
- class of fighters or weapon holder (chainsaw, sword, dagger)
- critical hits
