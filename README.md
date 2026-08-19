# RetroWPBL
The purpose of this project is to create a Retrosheet-like repository for Women's Pro Baseball League (WPBL) games, starting from the inaugural 2026 season. Most of the syntax is as expected for Retrosheet, hopefully making for something that can easily be plugged into a parser with minimal changes.

## Notes:
### General notes:
1. IDs here use number ranges not normally covered in Retrosheet files, in order to prevent any future conflict with Retrosheet people IDs:
"aaaaa2xx" IDs are players, akin to "aaaaa0xx" or "aaaaa1xx" IDs.
"aaaaa6xx" IDs are coaches/managers, akin to "aaaaa8xx" IDs.
"aaaaa7xx" IDs are umpires, akin to "aaaaa9xx" IDs.
The only exceptions are people who already exist (for example, many managers/coaches are former MLB players.) In such cases, the Retrosheet IDs are used but the MLB career timespans are ignored.
2. Without further information about scoring decisions, I have set team earned runs in gamelogs to be the same as earned runs.
### Event file notes:
1. Hit location is not widely provided yet since I do not have the means to automatically determine the position of batted balls in respect to stadium shapes/sizes. I am currently working to hopefully be able to provide this information.
2. Additional note to point 1: numbers after hits, as per Retrosheet, are the first fielder to reach the ball rather than hit location. For example, an S9 is a single to the right fielder but may be in center field.
3. Pitch blocking info ("*" in pitch sequences) is not present yet; I hope to be able to add it in the future.
### Biodata notes:
1. One crucial difference between Retrosheet's bio-data and the bio-data here is that rather than "BIRTH" info, I have "FROM" info. This may very well just be where the player is currently situated rather than where they were born. This is done because the WPBL provides direct info on where each player is from. I will look into changing this in the future.
2. Names are not shown with diacritics. This is keeping in line with Retrosheet biodata.
3. Biographical info is gathered piecemeal from online sources and may be inaccurate.
### Roster notes:
1. Although rosters are shown with 29-30 people in each, there is actually some nuance here. Active rosters are 15 people max, but players drafted by teams are restricted to playing for those teams in cases of, for example, injury. All drafted players are included as part of a sort of inactive roster even if they are not active.
2. The discrepancy in roster sizes can likely be traced to three people who were drafted but appear to have opted out of becoming part of their drafted teams' respective rosters, as well as one active player (Val Perez) who was not one of the drafted players but later signed.