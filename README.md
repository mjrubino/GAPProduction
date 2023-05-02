# GAPProduction
Code used for producing and managing GAP wildlife range maps and habitat models.  This package includes handy functions to save time performing many tedious tasks and it facilitates convenient interaction with the internal GAP database with Python.  It is for internal use and data development and is not usable to those without permission to access GAP databases.

# Functions

## Database
* ConnectToDB() - Provides a cursor within and a connection to the database
* GapCase() - Returns an input string in the Gap Code capitalization ('mAMROx')

## Taxonomy

## Ranges

## Conversions
Performs common area and length unit conversions

* CellsToHectares() -- Converts a 30m raster cell count to hectares
    
* CellsToAcres() -- Converts a 30m raster cell count to acres
    
* CellsToSqMeters() -- Converts a 30m raster cell count to square meters
    
* CellsToSqMiles() -- Converts a 30m raster cell count to square miles
    
* SqMetersToHectares() -- Converts square meters to hectares
    
* *SqMetersToSqMiles() -- Converts square meters to square miles
    
* SqMilesToHectares() -- Converts square miles to hectares
    
* SqMilesToAcres() -- Converts square miles to acres
    
* SqMilesToSqMeters() -- Converts square miles to square meters
    
* HectaresToAcres() -- Converts hectares to acres
    
* HectaresToSqMeters() -- Converts hectares to square meters
    
* HectaresToSqMiles() -- Converts hectares to square miles
    
* AcresToHectares() -- Converts acres to hectares
    
* AcresToSqMeters() -- Converts acres to square meters
    
* AcresToSqMiles() -- Converts acres to square miles
    
* MilesToMeters() -- Converts miles to meters
    
* MetersToMiles() -- Converts meters to miles
    
* MilesToKilometers() -- Converts miles to kilometers
    
* KilometersToMiles() -- Converts kilometers to miles

## Dictionaries
This module stores dictionaries commonly used in processing GAP data as well
as general functions for manipulating dictionaries.

* InvertDictionary() -- Returns a dictionary in which the keys are the values
          from the input dictionary, and the values are a list of keys that had
          that value in the input dictionary
    
* ReverseDictionary() -- Returns a dictionary in which the keys and values have
          been swapped.
    
* IterableOfIterablesToDictionary() - Converts a list/tuple of lists/tuples to a
          dictionary
    
        
* stateDict_To_Abbr -- A dictionary in which the keys are state/territory names
          and the values are the states' two-character postal code abbreviations.
    
* stateDict_From_Abbr -- A dictionary in which the keys are the states' two-
          character postal code abbreviations, and the values are the state names.
    
* taxaDict -- A dictionary in which the keys are the class letter, used as the
          the first character in the six-character GAP unique IDs for species, and
          the values are the class common name
    
* taxaDict_Latin -- A dictionary in which the keys are the class letter, used
          as the the first character in the six-character GAP unique IDs for
          species, and the values are the class scientific name
    
* stateFIPS_Code_to_Name -- A dictionary in which the keys are the state FIPS
          codes (as int) and the values are the state names
    
* stateFIPS_Name_to_Code -- A dictionary in which the keys are the state names
          and the values are the state FIPS codes (as int)
    
* regionsDict_Num_To_Name = A dictionary in which the keys are the GAP modeling
          regions by numerical code (as int) and the values are the names of the
          modeling regions
    
* regionsDict_Num_To_Abbr = A dictionary in which the keys are the GAP modeling
          regions by numerical code (as int) and the values are the abbreviations
          of the modeling regions
    
* regionsDict_Abbr_To_Num = A dictionary in which the keys are the GAP modeling
          region abbreviations and the values are the modeling region codes (as
          int)
    
* regionsDict_Name_To_Num = A dictionary in which the keys are the GAP modeling
          region names and the values are the modeling region codes (as int)
    
* regionsDict_Abbr_To_Name = A dictionary in which the keys are the GAP
          modeling region abbreviations and the vlaues are the modeling region
          names
    
* rangeCodesDict = A dictionary of dictionaries with a key for each GAP range map 
          attribute and a value that's a dictionary of definitions.
    
* staffDict = A dictionary of staff's initials.


## Docs
This module facilitates common tasks for searching/manipulating text files.

* Write() - appends to (default) or overwrites a file with the text of the second
      argument; creates the file and even the directories, if necessary.

* DocReplace() - replaces selected text in a given document; any number of text
      replacement pairs may be submitted.

* GetLines() - returns a list containing the complete text of every line that
      contains the search text

* SearchInFiles() - searches for the given text in the files of the given root
      directory, including all subdirectories

* SearchFilenames() - searches for the given text in the filenames of a given
      root directory, including all subdirectories

* SearchDirectoryNames() -- searches the given text in the directory names of
      given root directory, including all subdirectories


## Text Strings
Facilitates common tasks for searching and filtering lists, strings, etc.

* FilterList() -- Returns a list containing items from the input list that
match the search string.
* LegalChars() -- Returns the string with all illegal characters removed/replaced.
* RemoveRepeats() -- Returns the string with all adjacent, duplicate occurrences 
of the given search string reduced to a single occurrence.