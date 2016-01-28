# Api
Api Documentation for the new TF2Pickup.net website

## Api v1

The Pathprefix is /api/v1/



### Current Pickups
### Path: /current_pickups/:region

Allowed values for the region are: 'eu', 'na', 'au'

Example path: tf2pickup.net/api/v1/current_pickups/eu

This will return an array containing 4 Objects

#### type
Type: String
Description: The gamemode

#### maps
Type: Array containing three Strings
Description: The currently available maps

#### players
Type: Array containing objects
Each object contains:

##### name
Type: String
Desciption: The classname

##### count
Type: Number
Description: The currently signed up players

#####  link
Type: String
Description: The link to the slot


### User info
### /user/:steamId

Example path: tf2pickup.net/api/v1/user/76561198085010248

This will return an object with the following keys:

#### exists
Type: Boolean 
Description: Returns true or false, depends on if the user exists in our db

#### steamId
Type: String
Description: Returns the steamId, you provided in the url.  The steamId will always be returned even when the user doesn't exists

#### username
Type: String
Description: The username that will be displayed on TF2Pickup.net

#### region
Type: String
Description: The region that the user has selected

#### steamId3
Type: String
Description: The users steamId3

#### pickupsPlayed
Type: Number
Description: The number of pickups the user played

#### pickupsPlayedByClass
Type: Object
Description: An object containing the pickupsPlayed by an specific class.

#### link
Type: String
Descrition: The link to the users TF2Pickup.net profile
