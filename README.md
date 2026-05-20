# CIT4407 Assignment 2

## Task 1: Clean data
**Purpose:** check the input file first, if it satisfies the minimum requirements, then the script cleans the CSV file that can be used in the later analysis process.

### First, error checking
1. No input file specified
2. Input file not found in the current directory
3. Input file not in CSV format
4. Empty file provided
5. Incorrect number of columns (expects 7 columns)

### If no errors, then enter the cleaning process

**Before starting, separate header independently**
1. `$no_rating` - remove 7th colomn
2. `no_empty()` - Removes rows with empty fields
3. `no_repeated()` - Removes duplicate rows while preserving order
4. `no_zero()` - Removes rows with zero likes/dislikes
5. `fix_date()` - Strips time from datetime fields

**Feature:** Creating functions and piping them in the final step

**Method to execute:** `./clean trending_videos_unclean.csv`

---

## Task 2: Analyse data
**Purpose:** Based on the cleaned CSV file as input, this script fetches data via piping and finds specific information, and then illustrates the meaning of that information.

### Calculations Performed:

1. Most frequent video ID (highest occurrence count)
2. Mean number of views (2 decimal places)
3. Video ID with maximum dislikes
4. Video with highest engagement rate: (likes + dislikes)/views
5. Video with least net sentiment rate: (likes - dislikes)/views

**Feature:** Handles ties in Task 4 and Task 5 by creating a variable that covers all related information

**Method:** `./analyse trending_videos_clean.csv`