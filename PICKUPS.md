## Pickups Api

### Current pickups

/api/v1/pickups/:region

#### Route options

- region
  - Should be one of the following: eu, na or au

#### Examples

> api/v1/pickups/eu

This will return an array containing data for each gamemode

Each object in the array will have the following keys:

- type
  - The pickups type
  -  Values can be: 6v6, 9v9, bball, ultiduo
- currentPlayers
  - the current players that are currently in the pickup
- maps
  - An array containing the possible maps
- players
  - An array containing objects with info about the classes
  - Each Object will have the following keys:
    - name
      - The name of the class
      - Values: scout, soldier, pyro, demoman, heavy, engineer, medic, sniper, spy
    - currentPlayers
      - The current players that joined the class
    - maxPlayers
      - Maximal players that can join the class
    - link
      - A link to join the class
      -  This depends on the users region so if you are showing the eu pickups but the user has set his region to na he will join the na pickups