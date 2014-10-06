# Data Description

## Data category :
-------------
- createTime (timestamp of the event)
- user (user id)
- action (event name)
- userDomain (user Domain)
- userCountry (user Country ISO (3) code)
- st1|st2|st3 (category of the event; st1 distinguish between server/client events with suffic related to platform (eg. fb mean channel facebook))
- level
- value|value2|value3
- string1|string2|string3
- date1|date2
- data (additional event information)

## Event types:
------------
1. Technical Onboarding Funnel events
  1. activity/acquisition/install or activity/acquisition/click (infom about source via which user came to the game)
  2. guest-user
  3. user-login (server received logged user)
  4. connected
  5. events-ready (client received first event from the user server)
  6. init-texts (text are loaded)
  7. init-view (UI ready)
  8. check-version (version of the main SWF has been successfully verifed)
  9. tcp-enabled
  10. load-game (main module of flash game is loaded)
  11. invitation-info-ready (information about kind of user ivitation into the game)
  12. stage-3d-availability
  13. menu-enabled (user can interact with the game)
  14. load-page (all javascript libraries are loaded)
  15. page-info
  16. registration-bonus / daily-bonus
  17. session-start

2. Match events
  1. lobby-start / lobby-exit (player looking for the opponent)
  2. match-start (st3 category inform about type of match)
  3. shot
  4. select-pocket
  5. return-ball
  6. match-end
  7. match-summary

3. Shop events
  1. shop (enter to the shop)
  2. shop-cues-tour (browsing throuth the shop)
  3. shop-cues-national (browsing throuth the shop)
  4. shop-cues-purchased (browsing throuth the shop)
  5. shop-prints-recommended (browsing throuth the shop)
  6. shop-effects-recommended (browsing throuth the shop)
  7. shop-cues-recommended (browsing throuth the shop)
  8. shop-cues-tour (browsing throuth the shop)
  9. shop-buy (click buy the product eg cue)
  10. shop-buy-confirm (purchase confirmation)
  11. product-purchase (information about product)
  12. add-coins / add-gold (enter to coins / gold packages shop)

4. Menu events
5. Additional events

Sample session contain events for new user who came into game based on friend invite (via notification). After few matches (and rematches) user purchased cue (like product)| coins and gold packages.


createTime        |user      |action                      |userDomain       |userCountry|st1      |st2         |st3  |level|value    |value2|value3|string1|string2 |string3|date1  |date2  |data
------------------|----------|----------------------------|-----------------|-----------|---------|------------|-----|-----|---------|------|------|-------|--------|-------|-------|-------|-------------------------------
9/18/2014 12:29:28|8625560152|activity/acquisition/install|apps.facebook.com|CZE        |NULL     |NULL        |NULL |0    |0        |0     |0     |pool-3 |8C612FB9|NULL   |NULL   |NULL   |NULL
9/18/2014 12:29:28|8625560152|activity/acquisition/click  |apps.facebook.com|CZE        |facebook |notification|NULL |0    |0        |0     |0     |pool-3 |8C612FB9|partner|NULL   |NULL   |NULL
9/18/2014 12:29:28|8625560152|guest-user                  |apps.facebook.com|CZE        |script-fb|loading     |guest|0    |351615012|0     |0     |NULL   |NULL    |NULL   |NULL   |NULL   |NULL
9/18/2014 12:29:29|8625560152|user-login                  |apps.facebook.com|CZE        |xserver-x|loading     |NULL |0    |175      |171   |2     |Male   |19780321|CZE    |14:00.0|29:25.6|NULL
9/18/2014 12:29:29|8625560152|connected                   |apps.facebook.com|CZE        |game-fb  |loading     |NULL |0    |1980     |0     |0     |NULL   |NULL    |NULL   |NULL   |NULL   |"{""version"":""3.9.24696.4""}"
9/18/2014 12:29:29|8625560152|events-ready                |apps.facebook.com|CZE        |game-fb  |loading     |NULL |1    |2864     |0     |0     |NULL   |NULL    |NULL   |NULL   |NULL   |"{""version"":""3.9.24696.4""}"
9/18/2014 12:29:29|8625560152|init-texts                  |apps.facebook.com|CZE        |game-fb  |loading     |NULL |0    |2515     |0     |0     |NULL   |NULL    |NULL   |NULL   |NULL   |"{""version"":""3.9.24696.4""}"

Geewa's list of business problems: [TASKS](https://github.com/hackathonBI/Geewa/blob/master/Tasks.md).