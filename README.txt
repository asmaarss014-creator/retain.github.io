DARA PARTS DATABASE
===================

FILES
-----
parts_names.txt  = part names only; used for live autocomplete.
parts_data.txt   = detailed records; one record per part, separated by a blank line.
brands.txt       = optional brand list.
models.txt       = optional model list.
part_numbers.txt = optional part-number list.

ADDING A PART
-------------
1. Add the name to parts_names.txt if it is new.
2. In parts_data.txt, copy an existing record.
3. Give it a NEW unique PART_ID.
4. Fill in PART_NAME, BRAND, MODEL, YEAR and PART_NUMBER.
5. Fill in compatibility/specifications.
6. Leave unknown fields empty.
7. Save and reload the app.

RECORD FORMAT
-------------
PART_ID=000005
PART_NAME=Motherboard
BRAND=Dell
MODEL=Latitude E5450
YEAR=2015
PART_NUMBER=EXACT_NUMBER
TYPE=Motherboard
RAM=DDR3L
STORAGE=SATA
CPU_PLATFORM=5th Gen Intel Core
COMPATIBILITY=Dell Latitude E5450
CONDITION=Used/Tested
BUY_PRICE=1400 AFN
WHOLESALE_PRICE=1700 AFN
RETAIL_PRICE=2200 AFN
NOTES=Verify revision

RULES
-----
- PART_ID must be unique.
- Keep field names exactly as written.
- Put one record per physical part/listing.
- Copy part numbers exactly from labels/boards.
- Use separate records when revisions are not compatible.
- Prices can be changed without changing PART_ID.
- Back up the TXT files before large edits.

SEARCH
------
Box 1 searches PART_NAME and gives suggestions while typing.
Box 2 searches PART_NUMBER, PART_ID, MODEL and other record values.
Search can use either box or both.

The included index.html is a clean offline-style UI prototype.
It reads the TXT files directly. For browser security, run it through a
small local web server rather than opening index.html directly as file://.

For a future Android version, these same TXT files can be bundled with the
APK or imported into SQLite for much larger databases.
