<p align="center">
  <h1 align="center">Unofficial Hyperscape API Documentation<br>By Tabstats.com</h3>
</p>

<hr>

## Limitations
- There are no limitations to this API as long as it is not abused. We hold the right to refuse service to anyone who we believe is abusing this system.

<hr>

## Search by name

Request URL {GET} https://hypers.apitab.com/search/{platform}/{playername}

PATH | **platform**:

- <i>**uplay**</i> will only display PC players<br>
- <i>**psn**</i> will only display Playstation players<br>
- <i>**xbl**</i> will only display Xbox players<br>

PATH | **playername**:

- <i>**playername**</i> urlencode the playername<br>

PARAMETER | **u**:

- <i>**unix**</i> provide the unix timestamp to avoid caching

#### Response Data:

- <i>**platform**</i> is the platform searched<br>
- <i>**searchq**</i> is the requested player name sent to the API<br>
- <i>**players**</i> is a `JSON` object containing ubisoft player IDs with their own JSON Objects<br>

#### Players Object:
<i> **profile**</i>
- <i>**p_id**</i> is the identifier assigned by ubisoft to the player.<br>
- <i>**p_name**</i> is the current name of the player<br>
- <i>**p_user**</i> is the identifier assigned by ubisoft to the player.<br>
- <i>**p_platform**</i> is the platform of the player<br>
- <i>**verified**</i> is a `boolean` depicting if the player is verified<br>

Example: https://hypers.apitab.com/search/uplay/baiier?u=89031276

Example response: <u>[Click Here](https://github.com/Tabwire/HyperScape-API/blob/master/responses/playerdatabyname.json)</u>

<hr>

## Get player data by ID

Request URL {GET} https://hypers.apitab.com/player/{p_id}?u=89031276

PATH | **p_id**:

- <i>**playerid**</i> is the ID that Ubisoft assigns to every player.<br>

PARAMETER | **u**:

- <i>**unix**</i> provide the unix timestamp to avoid caching

An example of a player ID is: <i>**43eccd4d-1fb4-47b7-bfe5-5167fa48a945**</i>

Example: https://hypers.apitab.com/player/43eccd4d-1fb4-47b7-bfe5-5167fa48a945?u=89031276

Example response: <u>[Click Here](https://github.com/Tabwire/HyperScape-API/blob/master/responses/playerdatabyid.json)</u>

<hr>

## Update player data by ID

Request URL {GET} https://hypers.apitab.com/update/{p_id}?u=89031276

PATH | **p_id**:
- <i>**playerid**</i> is the ID that Ubisoft assigns to every player.<br>

Please note that 600 seconds is need to pass for the profile to refresh. If an update request is sent sooner, the request will redirect.

<hr>

## Affiliation
- The Hyperscape API is in no way shape or form affiliated with Ubisoft and its partners. Any "Hyperscape" name, logos and/or images are registered trademarks of Ubisoft.
