# RetroWPBL
The purpose of this project is to create a Retrosheet-like repository for WPBL games. Most of the syntax is as expected, hopefully making for something that can easily be plugged into a parser with minimal changes.

## Notes:
### General notes:
1. IDs here use number ranges not normally covered in Retrosheet files, in order to prevent any future conflict with Retrosheet people IDs:
"aaaaa2xx" IDs are players, akin to "aaaaa0xx" or "aaaaa1xx" IDs.
"aaaaa6xx" IDs are coaches/managers, akin to "aaaaa8xx" IDs.
"aaaaa7xx" IDs are umpires, akin to "aaaaa9xx" IDs.
The only exceptions are people who already exist (for example, many managers/coaches are former MLB players.) In such cases, the IDs are used but the MLB career timespans are ignored.
2. Although rosters are shown with 29-30 people in each, there is actually some nuance here. Rosters are 15 people max, but players drafted by teams are restricted to playing for those teams in cases of, for example, injury. All drafted players are included even if they are not technically on the roster.
3. I originally included pitch blocking info ("*" in pitch sequences). I have removed this since I do not have a clear idea of what constitutes the standard for a blocked pitch in Retrosheet, and any information I could include would not particularly informative.
### Biodata notes:
1. One crucial difference between Retrosheet's bio-data and the bio-data here is that rather than "BIRTH" info, I have "FROM" info. This may very well just be where the player is currently situated. This is done because the WPBL provides direct info on where each player is from, which makes it a lot more convenient than finding where people were born. I will look into changing this in the future.
2. Names are not shown with diacritics. This is keeping in line with Retrosheet biodata.
3. Biographical data is gathered piecemeal from online sources and may be inaccurate.