# Summary Level Naming and Hierarchical Access Changes

## Impetus

The Bureau's API program is expanding in reach, it has become necessary to label geographic concepts more precisely in order to ensure as little confusion regarding what these geographies are actually referring to. Primary candidates in need of greater specificity are any geographic "Summary Level" which may be represented as either whole or "part" of its standard boundary definition (its entirety).

For geographies which may refer to either a whole or a part, these summary levels - along with the manner by which you currently access them hierarchically - will be changing. 

## Contact Us

If you have any questions/concerns about this process or the meanings of the concepts that follow, please get in touch with us via one of our outreach channels:

- Join us on [Slack](https://join.slack.com/t/uscensusbureau/shared_invite/enQtMjQ3NzUyNTM3NDU3LTZmNGI1MmQzY2Y2ZTU1ODJhNDQwMmY2YmZiNmFkNzg4YmJkYmQzZjQyNDhkNDYxN2JhYjkxZDEwMGI2OGU5NzQ)
- Join us on [gitter.im](https://gitter.im/uscensusbureau/general)
- Send an email to: cnmp.developers.list@census.gov

# Change Matrix 

We are providing the following change matrix to assist you in this transition.

## Important Example of the Meaning of Summary Levels: 

It may cause some confusion that (for example) `block group` seems to be changing to `block group (or part)`, but do not worry. If your intention is to use `block group` as the geography of your analysis, that summary level (`150`) will not be changing. However, if your intention is to use a `block group` as a member of a `county subdivision` (summary level `091`), some of these block groups are - therein - incomplete, thus `(or part)` becomes a necessary qualifier of that summary level for use via API.

You can find a complete list of all [changing Summary Levels at the bottom](#summary-level-index) of this document.

# Geography (`for` predicate) Changes

## County Access

Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
155, 282, 285, 288, 362, 365, 622, 881 | county                                                   | county (or part)
261, 265, 267, 613, 623 | county subdivision                                                      | county subdivision (or part)


## Tract Access


Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
080, 158, 631, 636 | census tract                                                                 | tract (or part)
 
## Block Group Access


Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
091           | block group                                                                       | block group (or part)

## Place Access

Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
070, 263, 266, 268, 614, 624| place/remainder                                                     | place/remainder (or part)
172, 542      | place within consolidated city                                                    | place (or part)
644, 645      | place within consolidated city                                                    | place/remainder (or part)


## MSA Access

Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
320, 341      | metropolitan statistical area/micropolitan statistical area                       | metropolitan statistical area/micropolitan statistical area (or part)


## ZCTA Access

Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
871           | zip code tabulation area                                                          | zip code tabulation area (or part)

## Pricipal City Access

Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
321           | principal city                                                                    | principal city (or part)

## Metropolitan Division Access

Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
323           | metropolitan division                                                             | metropolitan division (or part)

## CSA Access

Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
340           | combined statistical area                                                         | combined statistical area (or part)

## New England Area Access

Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
345           | combined new england city and town area                                           | combined new england city and town area (or part)
346, 360      | new england city and town area                                                    | new england city and town area (or part)
364           | necta division                                                                    | necta division (or part)

## Consolidated City Access

Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
541, 615, 625 | consolidated city                                                                 | consolidated city (or part)


## Alaska Native Regional Corporation Access

Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
634, 639      | alaska native regional corporation                                                | alaska native regional corporation (or part)


## Tribal Subdivision Access

Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
281, 284, 287, 553, 554, 555 | tribal subdivision/remainder                                       | tribal subdivision/remainder (or part)


## American Indian Access

Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
144, 154      | american indian area/alaska native area/hawaiian home land                        | american indian area/alaska native area/hawaiian home land (or part)
280, 616, 626 | american indian area/alaska native area/hawaiian home land                        | american indian area/alaska native area/hawaiian home land (or part)
283, 551, 646, 647 | american indian area/alaska native area(reservation or statistical entity only)   | american indian area/alaska native area (reservation or statistical entity only) (or part)
286, 648, 649 | american indian area (off-reservation trust land only)/hawaiian home land         | american indian area (off-reservation trust land only)/hawaiian home land (or part)
552           | "american indian area (off-reservation trust land only)/hawaiian home land"       | "american indian area/alaska native area/hawaiian home land (or part)"

# Geographic Hierarchy (`in` & `for` predicate) Changes

## New American Indian Access Hierarchies

#### 265
Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
...           | "state"                                                                           | "state"
...           | "american indian area/alaska native area (reservation or statistical entity only)"| "american indian area/alaska native area/hawaiian home land (or part)"
...           | "county"                                                                          | "american indian area/alaska native area (reservation or statistical entity only) (or part)"
265           |                                                                                   | "county (or part)"
  
#### 266
Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
...           | "state"                                                                           | "state"
...           | "american indian area/alaska native area (reservation or statistical entity only)"| "american indian area/alaska native area/hawaiian home land (or part)"
...           | "county subdivision"                                                              | "american indian area/alaska native area (reservation or statistical entity only) (or part)"
266           |                                                                                   | "county subdivision (or part)"

#### 267
Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
...           | "state"                                                                           | "state"
...           | "american indian area (off-reservation trust land only)/hawaiian home land"       | "american indian area/alaska native area/hawaiian home land (or part)"
...           | "county"                                                                          | "american indian area (off-reservation trust land only)/hawaiian home land (or part)"
267           |                                                                                   | "county (or part)"

#### 268
Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
...           | "state"                                                                           | "state"
...           | "american indian area (off-reservation trust land only)/hawaiian home land"       | "american indian area/alaska native area/hawaiian home land (or part)"
...           | "county"                                                                          | "american indian area (off-reservation trust land only)/hawaiian home land (or part)"
...           | "county subdivision"                                                              | "county (or part)"
268           |                                                                                   | "county subdivision (or part)"

#### 283
Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
...           | "state"                                                                           | "state"
283           |                                                                                   | "american indian area/alaska native area/hawaiian home land (or part)"

#### 284
Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
...           | "state"                                                                           | "state"
...           | "american indian area (reservation or statistical entity only)"                   | "american indian area/alaska native area/hawaiian home land (or part)"
284           |                                                                                   | "american indian area/alaska native area (reservation or statistical entity only) (or part)"

#### 285
Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
...           | "state"                                                                           | "state"
...           | "american indian area (reservation or statistical entity only)"                   | "american indian area/alaska native area/hawaiian home land (or part)"
285           |                                                                                   | "american indian area/alaska native area (reservation or statistical entity only) (or part)"

#### 286
Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
...           | "state"                                                                           | "state"
286           |                                                                                   | "american indian area/alaska native area/hawaiian home land (or part)"

#### 287
Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
...           | "state"                                                                           | "state"
...           | "american indian area (off-reservation trust land only)"                          | "american indian area/alaska native area/hawaiian home land (or part)"
287           |                                                                                   | "american indian area (off-reservation trust land only)/hawaiian home land (or part)"

#### 288
Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
...           | "state"                                                                           | "state"
...           | "american indian area (off-reservation trust land only)/hawaiian home land"       | "american indian area/alaska native area/hawaiian home land (or part)"
288           |                                                                                   | "american indian area (off-reservation trust land only)/hawaiian home land (or part)"

#### 551 & 552
Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
...           | "state"                                                                           | "state"
...           | "congressional district"                                                          | "congressional district"
551, 552      |                                                                                   | "american indian area (off-reservation trust land only)/hawaiian home land (or part)"

#### 554
Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
...           | "state"                                                                           | "state"
...           | "congressional district"                                                          | "congressional district"
...           | "american indian area (reservation or statistical entity only)"                   | "american indian area (off-reservation trust land only)/hawaiian home land (or part)"
554           |                                                                                   | "american indian area/alaska native area (reservation or statistical entity only) (or part)"

#### 555
Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
...           | "state"                                                                           | "state"
...           | "congressional district"                                                          | "congressional district"
...           | "american indian area (off-reservation trust land only)"                          | "american indian area/alaska native area/hawaiian home land (or part)"
555           |                                                                                   | "american indian area (off-reservation trust land only)/hawaiian home land (or part)"

#### 646 & 648
Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
...           | "state"                                                                           | "state"
...           | "state legislative district (upper chamber)"                                      | "state legislative district (upper chamber)"
646, 648      |                                                                                   | "american indian area/alaska native area/hawaiian home land (or part)"

#### 647 & 649
Summary Levels| Old Access Hierarchy and/or Name                                                  | New Access Hierarchy and/or Name
------------- | --------------------------------------------------------------------------------- | -----------------------------
...           | "state"                                                                           | "state"
...           | "state legislative district (lower chamber)"                                      | "state legislative district (lower chamber)"
647, 649      |                                                                                   | "american indian area/alaska native area/hawaiian home land (or part)"






# Summary Level Index


 Summary Level | 2010 Decennial Geographic Hierarchy and/or Name                                                                  | Changing in 2017
:---:| -------------------------------------------------------------------------------------------------------------------------------------- | :---:
 010 | United States                                                                                                                          | 
 020 | Region                                                                                                                                 |
 030 | Division                                                                                                                               |
 040 | State                                                                                                                                  |
 050 | State-County                                                                                                                           |
 060 | State-County-County Subdivision                                                                                                        |
 067 | State-County-County Subdivision-Subminor Civil Division                                                                                |
 070 | State-County-County Subdivision-Place/Remainder                                                                                        | ✓
 080 | State-County-County Subdivision-Place/Remainder-Census Tract                                                                           | ✓
 091 | State-County-County Subdivision-Place/Remainder-Census Tract-Block Group                                                               | ✓
 101 | State-County-County Sub∀division-Place/Remainder-Census Tract∀-Block Group-Block                                                       |
 140 | State-County-Census Tract                                                                                                              |
 144 | State-County-Census Tract-American Indian Area/Alaska Native Area/Hawaiian Home Land                                                   | ✓
 150 | State-County-Census Tract-Block Group                                                                                                  |
 154 | State-County-Census Tract-Block Group-American Indian Area/Alaska Native Area/Hawaiian Home Land                                       | ✓
 155 | State-Place-County                                                                                                                     | ✓
 158 | State-Place-County-Census Tract                                                                                                        | ✓
 160 | State-Place                                                                                                                            |
 170 | State-Consolidated City                                                                                                                |
 172 | State-Consolidated City-Place Within Consolidated City                                                                                 | ✓
 230 | State-Alaska Native Regional Corporation                                                                                               |
 250 | American Indian Area/Alaska Native Area/Hawaiian Home Land                                                                             |
 251 | American Indian Area-Tribal Subdivision/Remainder                                                                                      |
 252 | American Indian Area/Alaska Native Area (Reservation or Statistical Entity Only)                                                       |
 253 | American Indian Area (Reservation or Statistical Entity Only)-Tribal Subdivision/Remainder                                             |
 254 | American Indian Area (Off-Reservation Trust Land Only)/Hawaiian Home Land                                                              |
 255 | American Indian Area (Off-Reservation Trust Land Only)-Tribal Subdivision/Remainder                                                    |
 256 | American Indian Area-Tribal Census Tract                                                                                               |
 257 | American Indian Area-Tribal Subdivision/Remainder-Tribal Census Tract                                                                  |
 258 | American Indian Area-Tribal Census Tract-Tribal Block Group                                                                            |
 259 | American Indian Area-Tribal Subdivision/Remainder-Tribal Census Tract-Tribal Block Group                                               |
 260 | American Indian Area/Alaska Native Area/Hawaiian Home Land-State                                                                       |
 261 | State-American Indian Area/Alaska Native Area/Hawaiian Home Land-County-County Subdivision                                             | ✓
 262 | American Indian Area/Alaska Native Area (Reservation or Statistical Entity Only)-State                                                 |
 263 | State-American Indian Area/Alaska Native Area/Hawaiian Home Land-County-County Subdivision-Place/Remainder                             | ✓
 264 | American Indian Area (Off-Reservation Trust Land Only)/Hawaiian Home Land-State                                                        |
 265 | State-American Indian Area/Alaska Native Area (Reservation or Statistical Entity Only)-County-County Subdivision                       | ✓
 266 | State-American Indian Area/Alaska Native Area (Reservation or Statistical Entity Only)-County-County Subdivision-Place/Remainder       | ✓
 267 | State-American Indian Area (Off-Reservation Trust Land Only)/Hawaiian Home Land-County-County Subdivision                              | ✓
 268 | State-American Indian Area (Off-Reservation Trust Land Only)/Hawaiian Home Land-County-County Subdivision-Place/Remainder              | ✓
 269 | American Indian Area/Alaska Native Area/Hawaiian Home Land-State-Place/Remainder                                                       |
 270 | American Indian Area/Alaska Native Area/Hawaiian Home Land-State-County                                                                |
 271 | American Indian Area/Alaska Native Area/Hawaiian Home Land-State-County-County Subdivision                                             |
 272 | American Indian Area/Alaska Native Area (Reservation or Statistical Entity Only)-State-County                                          |
 273 | American Indian Area/Alaska Native Area/Hawaiian Home Land-State-County-County Subdivision-Place/Remainder                             |
 274 | American Indian Area (Off-Reservation Trust Land Only)/Hawaiian Home Land-State-County                                                 |
 275 | American Indian Area/Alaska Native Area (Reservation or Statistical Entity Only)-State-County-County Subdivision                       |
 276 | American Indian Area/Alaska Native Area (Reservation or Statistical Entity Only)-State-County-County Subdivision-Place/Remainder       |
 277 | American Indian Area (Off-Reservation Trust Land Only)/Hawaiian Home Land-State-County-County Subdivision                              |
 278 | American Indian Area (Off-Reservation Trust Land Only)/Hawaiian Home Land-State-County-County Subdivision-Place/Remainder              |
 280 | State-American Indian Area/Alaska Native Area/Hawaiian Home Land                                                                       | ✓
 281 | State-American Indian Area-Tribal Subdivision/Remainder                                                                                | ✓
 282 | State-American Indian Area/Alaska Native Area/Hawaiian Home Land-County                                                                | ✓
 283 | State-American Indian Area/Alaska Native Area (Reservation or Statistical Entity Only)                                                 | ✓
 284 | State-American Indian Area (Reservation or Statistical Entity Only)-Tribal Subdivision/Remainder                                       | ✓
 285 | State-American Indian Area/Alaska Native Area (Reservation or Statistical Entity Only)-County                                          | ✓
 286 | State-American Indian Area (Off-Reservation Trust Land Only)/Hawaiian Home Land                                                        | ✓
 287 | State-American Indian Area (Off-Reservation Trust Land Only)-Tribal Subdivision/Remainder                                              | ✓
 288 | State-American Indian Area (Off-Reservation Trust Land Only)/Hawaiian Home Land-County                                                 | ✓
 290 | American Indian Area-Tribal Subdivision/Remainder-State                                                                                |
 291 | American Indian Area (Reservation Only)-Tribal Census Tract                                                                            |
 292 | American Indian Area (Off-Reservation Trust Land Only)-Tribal Census Tract                                                             |
 293 | American Indian Area (Reservation Only)-Tribal Census Tract-Tribal Block Group                                                         |
 294 | American Indian Area (Off-Reservation Trust Land Only)-Tribal Census Tract-Tribal Block Group                                          |
 310 | Metropolitan Statistical Area/Micropolitan Statistical Area                                                                            |
 311 | Metropolitan Statistical Area/Micropolitan Statistical Area-State                                                                      |
 312 | Metropolitan Statistical Area/Micropolitan Statistical Area-State-Principal City                                                       |
 313 | Metropolitan Statistical Area/Micropolitan Statistical Area-State-County                                                               |
 314 | Metropolitan Statistical Area/Micropolitan Statistical Area-Metropolitan Division                                                      |
 315 | Metropolitan Statistical Area/Micropolitan Statistical Area-Metropolitan Division-State                                                |
 316 | Metropolitan Statistical Area/Micropolitan Statistical Area-Metropolitan Division-State-County                                         |
 320 | State-Metropolitan Statistical Area/Micropolitan Statistical Area                                                                      | ✓
 321 | State-Metropolitan Statistical Area/Micropolitan Statistical Area-Principal City                                                       | ✓
 322 | State-Metropolitan Statistical Area/Micropolitan Statistical Area-County                                                               |
 323 | State-Metropolitan Statistical Area-Metropolitan Division                                                                              | ✓
 324 | State-Metropolitan Statistical Area-Metropolitan Division-County                                                                       |
 330 | Combined Statistical Area                                                                                                              |
 331 | Combined Statistical Area-State                                                                                                        |
 332 | Combined Statistical Area-Metropolitan Statistical Area/Micropolitan Statistical Area                                                  |
 333 | Combined Statistical Area-Metropolitan Statistical Area/Micropolitan Statistical Area-State                                            |
 335 | Combined New England City and Town Area                                                                                                |
 336 | Combined New England City and Town Area-State                                                                                          |
 337 | Combined New England City and Town Area-New England City and Town Area                                                                 |
 338 | Combined New England City and Town Area-New England City and Town Area-State                                                           |
 340 | State-Combined Statistical Area                                                                                                        | ✓
 341 | State-Combined Statistical Area-Metropolitan Statistical Area/Micropolitan Statistical Area                                            | ✓
 345 | State-Combined New England City and Town Area                                                                                          | ✓
 346 | State-Combined New England City and Town Area-New England City and Town Area                                                           | ✓
 350 | New England City and Town Area                                                                                                         |
 351 | New England City and Town Area-State                                                                                                   |
 352 | New England City and Town Area-State-Principal City                                                                                    |
 353 | New England City and Town Area-State-County                                                                                            |
 354 | New England City and Town Area-State-County-County Subdivision                                                                         |
 355 | New England City and Town Area (NECTA)-NECTA Division                                                                                  |
 356 | New England City and Town Area (NECTA)-NECTA Division-State                                                                            |
 357 | New England City and Town Area (NECTA)-NECTA Division-State-County                                                                     |
 358 | New England City and Town Area (NECTA)-NECTA Division-State-County-County Subdivision                                                  |
 360 | State-New England City and Town Area                                                                                                   | ✓
 361 | State-New England City and Town Area-Principal City                                                                                    |
 362 | State-New England City and Town Area-County                                                                                            | ✓
 363 | State-New England City and Town Area-County-County Subdivision                                                                         |
 364 | State-New England City and Town Area (NECTA)-NECTA Division                                                                            | ✓
 365 | State-New England City and Town Area (NECTA)-NECTA Division-County                                                                     | ✓
 366 | State-New England City and Town Area (NECTA)-NECTA Division-County-County Subdivision                                                  |
 500 | State-Congressional District                                                                                                           |
 510 | State-Congressional District-County                                                                                                    |
 511 | State-Congressional District-County-Census Tract                                                                                       |
 512 | State-County-Congressional District                                                                                                    |
 521 | State-Congressional District-County-County Subdivision                                                                                 |
 531 | State-Congressional District-Place/Remainder                                                                                           |
 532 | State-Place-Congressional District                                                                                                     |
 541 | State-Congressional District-Consolidated City                                                                                         | ✓
 542 | State-Congressional District-Consolidated City-Place Within Consolidated City                                                          | ✓
 550 | State-Congressional District-American Indian Area/Alaska Native Area/Hawaiian Home Land                                                |
 551 | State-Congressional District-American Indian Area/Alaska Native Area (Reservation or Statistical Entity Only)                          | ✓
 552 | State-Congressional District-American Indian Area (Off-Reservation Trust Land Only)/Hawaiian Home Land                                 | ✓
 553 | State-Congressional District-American Indian Area-Tribal Subdivision/Remainder                                                         | ✓
 554 | State-Congressional District-American Indian Area (Reservation or Statistical Entity Only)-Tribal Subdivision/Remainder                | ✓
 555 | State-Congressional District-American Indian Area (Off-Reservation Trust Land Only)-Tribal Subdivision/Remainder                       | ✓
 560 | State-Congressional District-Alaska Native Regional Corporation                                                                        |
 570 | State-Congressional District-School District (Elementary)/Remainder                                                                    |
 571 | State-Congressional District-School District (Secondary)/Remainder                                                                     |
 572 | State-Congressional District-School District (Unified)/Remainder                                                                       |
 610 | State⌀State Legislative District (Upper Chamber)                                                                                       |
 612 | State-State Legislative District (Upper Chamber)-County                                                                                |
 613 | State-State Legislative District (Upper Chamber)-County-County Subdivision                                                             | ✓
 614 | State-State Legislative District (Upper Chamber)-Place/Remainder                                                                       | ✓
 615 | State-State Legislative District (Upper Chamber)-Consolidated City                                                                     | ✓
 616 | State-State Legislative District (Upper Chamber)-American Indian Area/Alaska Native Area/Hawaiian Home Land                            | ✓
 617 | State-State Legislative District (Upper Chamber)-School District (Elementary)/Remainder                                                |
 618 | State-State Legislative District (Upper Chamber)-School District (Secondary)/Remainder                                                 |
 619 | State-State Legislative District (Upper Chamber)-School District (Unified)/Remainder                                                   |
 620 | State⌀State Legislative District (Lower Chamber)                                                                                       |
 622 | State-State Legislative District (Lower Chamber)-County                                                                                | ✓
 623 | State-State Legislative District (Lower Chamber)-County-County Subdivision                                                             | ✓
 624 | State-State Legislative District (Lower Chamber)-Place/Remainder                                                                       | ✓
 625 | State-State Legislative District (Lower Chamber)-Consolidated City                                                                     | ✓
 626 | State-State Legislative District (Lower Chamber)-American Indian Area/Alaska Native Area/Hawaiian Home Land                            | ✓
 627 | State-State Legislative District (Lower Chamber)-School District (Elementary)/Remainder                                                |
 628 | State-State Legislative District (Lower Chamber)-School District (Secondary)/Remainder                                                 |
 629 | State-State Legislative District (Lower Chamber)-School District (Unified)/Remainder                                                   |
 630 | State-State Legislative District (Upper Chamber)-County-Voting District/Remainder                                                      |
 631 | State-State Legislative District (Upper Chamber)-County-Census Tract                                                                   | ✓
 632 | State-State Legislative District (Upper Chamber)-County-County Subdivision-Subminor Civil Division                                     |
 633 | State-State Legislative District (Upper Chamber)-American Indian Area-Tribal Subdivision/Remainder                                     |
 634 | State-State Legislative District (Upper Chamber)-Alaska Native Regional Corporation                                                    | ✓
 635 | State-State Legislative District (Lower Chamber)-County-Voting District/Remainder                                                      |
 636 | State-State Legislative District (Lower Chamber)-County-Census Tract                                                                   | ✓
 637 | State-State Legislative District (Lower Chamber)-County-County Subdivision-Subminor Civil Division                                     |
 638 | State-State Legislative District (Lower Chamber)-American Indian Area-Tribal Subdivision/Remainder                                     |
 639 | State-State Legislative District (Lower Chamber)-Alaska Native Regional Corporation                                                    | ✓
 640 | State-County-State Legislative District (Upper Chamber)                                                                                |
 641 | State-County-State Legislative District (Lower Chamber)                                                                                |
 642 | State-Place-State Legislative District (Upper Chamber)                                                                                 |
 643 | State-Place-State Legislative District (Lower Chamber)                                                                                 |
 644 | State-State Legislative District (Upper Chamber)-Consolidated City-Place Within Consolidated City                                      | ✓
 645 | State-State Legislative District (Lower Chamber)-Consolidated City-Place Within Consolidated City                                      | ✓
 646 | State-State Legislative District (Upper Chamber)-American Indian Area/Alaska Native Area (Reservation or Statistical Entity Only)      | ✓
 647 | State-State Legislative District (Lower Chamber)-American Indian Area/Alaska Native Area (Reservation or Statistical Entity Only)      | ✓
 648 | State-State Legislative District (Upper Chamber)-American Indian Area (Off-Reservation Trust Land Only)/Hawaiian Home Land             | ✓
 649 | State-State Legislative District (Lower Chamber)-American Indian Area (Off-Reservation Trust Land Only)/Hawaiian Home Land             | ✓
 700 | State⌀County⌀Voting District/Remainder                                                                                                |
 701 | State-County-Voting District/Remainder-Place/Remainder                                                                                 |
 702 | State-County-Voting District/Remainder-Consolidated City                                                                               |
 703 | State-County-Voting District/Remainder-American Indian Area/Alaska Native Area/Hawaiian Home Land                                      |
 704 | State-County-Voting District/Remainder-American Indian Area-Tribal Subdivision/Remainder                                               |
 705 | State-County-Voting District/Remainder-Alaska Native Regional Corporation                                                              |
 706 | State-County-Voting District/Remainder-School District (Elementary)/Remainder                                                          |
 707 | State-County-Voting District/Remainder-School District (Secondary)/Remainder                                                           |
 708 | State-County-Voting District/Remainder-School District (Unified)/Remainder                                                             |
 709 | State-County-Voting District/Remainder-Census Tract                                                                                    |
 710 | State⌀County⌀Voting District/Remainder⌀County Subdivision                                                                             |
 715 | State-County-Voting District/Remainder-County Subdivision-Subminor Civil Division                                                      |
 720 | State⌀County⌀Voting District/Remainder⌀County Subdivision⌀Place/Remainder                                                            |
 730 | State⌀County⌀Voting District/Remainder⌀County Subdivision-Place/Remainder⌀Census Tract                                               |
 735 | State-County-Voting District/Remainder-County Subdivision-Subminor Civil Division-Census Tract                                         |
 740 | State⌀County⌀Voting District/Remainder⌀County Subdivision⌀Place/Remainder⌀Census Tract⌀Block Group                                   |
 745 | State-County-Voting District/Remainder-County Subdivision-Subminor Civil Division-Census Tract-Block Group                             |
 750 | State⌀County⌀Voting District/Remainder⌀County Subdivision⌀Place/Remainder-Census Tract-Block Group⌀Block                             |
 755 | State-County-Voting District/Remainder-County Subdivision-Subminor Civil Division-Census Tract-Block Group-Block                       |
 860 | 5-Digit ZIP Code Tabulation Area                                                                                                       |
 870 | 5-Digit ZIP Code Tabulation Area-State                                                                                                 |
 871 | State-5-Digit ZIP Code Tabulation Area                                                                                                 | ✓
 880 | 5-Digit ZIP Code Tabulation Area-State-County                                                                                          |
 881 | State-5-Digit ZIP Code Tabulation Area-County                                                                                          | ✓
 950 | State-School District (Elementary)/Remainder                                                                                           |
 960 | State-School District (Secondary)/Remainder                                                                                            |
 970 | State-School District (Unified)/Remainder                                                                                              |
                                                                                                                                                                  