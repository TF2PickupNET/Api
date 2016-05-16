## Servers Api

/api/v1/servers/:region

#### Route options

- region
  - The region(s) you want the server info from
  - Values: eu, na, au
  - You can pass in multiple regions by seperating them by commas

#### Examples:

Only one user:
> /api/v1/servers/eu

Multiple users:
> /api/v1/servers/eu,na

Both examples will return an array with objects containing info about the servers

Each object will have the following keys:

- label
  - The Label for the server
- ip
  - The ip of the server
- port
  - The port of the server
- connect
  - Steam connect link
- region
  - Where the server is located
- players
  - The current players
- map
  - The currently played map
- maxPlayers
  - the max players (might be 8 (DM) or 24 (MGE))