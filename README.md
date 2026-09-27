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
1. Adding hit location is in progress; I do not have the means to automatically determine the position of batted balls in respect to stadium shapes/sizes, so judgments are manual.
2. Additional note to point 1: numbers after hits, as per Retrosheet, are the first fielder to reach the ball rather than hit location. For example, an S9 is a single to the right fielder but may be in center field.
3. Pitch blocking info ("*" in pitch sequences) is not present yet; I hope to be able to add it in the future.
### Biodata notes:
1. One crucial difference between Retrosheet's bio-data and the bio-data here is that rather than "BIRTH" info, I have "FROM" info. This may very well just be where the player is currently situated rather than where they were born. This is done because the WPBL provides direct info on where each player is from. I will look into changing this in the future.
2. Names are not shown with diacritics. This is keeping in line with Retrosheet biodata.
3. Biographical info is gathered piecemeal from online sources and may be inaccurate.

## How information is gathered
I go through a standardized process:
1. I watch and score all games live directly in the event file, making notes of plays that I have either missed or that need to be reviewed later.
2. I go through archived game footage on Youtube and fill in said missing information.
3. I cross reference with official PBP (as of the last week of the 2026 regular season, the official WPBL stats site is no longer publicly available, and thus I use [SportyDolphin's website](sportydolphin.fun) as a proxy), checking for discrepancies in listed events, runner advances, or pitch sequences.
4. I once again go through game footage to compare, amending incorrect information either on my part or in official scoring, and making notes as needed. Note that, following the end of the season, I have begun collating information into a specific [discrepancies CSV file](./discrepancies.csv).
5. Once events are verified, I fill out game metadata. Temperature data - if not explicitly given on broadcast - is taken from Weather Underground historic data of Springfield. Sky, precipitation, wind direction, and field condition are visually confirmed by feed. Game time is from first pitch to last out.
6. I then construct game logs and box scores from event files.

## What aligns with and what differs from official data
The following are meant to line up exactly with official PBP:
1. Batted ball rulings (hits, fielder's choice, and errors)
2. RBI and unearned run assignments

The following are not necessarily meant to line up, instead being independently verified:
1. Assists and putouts
2. Runner advances
3. Pitch data