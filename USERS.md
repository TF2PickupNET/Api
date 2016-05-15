## Users Api

#### Route options

/api/v1/users/:steamIds

- SteamIds should be steamId64s
- You can pass in multiple steamIds by seperating them by commas
 
#### Examples:
 
Only one user:
> /api/v1/users/123
 
Multiple users:
> /api/v1/users/123,456,789
 
Both examples will return an array with the userdata

Each object will have the following keys:

- steamId64 (SteamID 64 of the user)
- steamId3 (SteamID 3 of the user)
- etf2lId (ETF2l id of the user)
  - Will be null if the user doesn't have an etf2l profile
- eseaId (ESEA id of the user)
  - Will be null if the user doesn't have an esea profile
- ugcLink (Url to the users uhc page)
  - Will be null if the user doesn't have an ugc profile
- region (The users region, can be eu, na or au)
- username (The users name)
- customSteamUrl (The custom steam url of the user)
- isDonator (If the user is a donator)
