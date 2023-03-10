# ArchivesSpace Technical Advisory Council
## Metadata Standards Sub-Team

### Example Encoded Archival Description (EAD) Documents

Within this repository, members of the Metadata Standards Sub-Team track
examples of [EAD Documents](https://www.loc.gov/ead/) used for 
testing importation and the extraction of metadata within ArchivesSpace.

The repository also includes a number of dedicated test files.

### EAD2002 Import Gotchas

______________________
extent and physdesc
______________________

- extent on the collection level is required
- extent may not contain commas
- physdesc should have @altrender
- extent should have @altrender
- extent should have @unit
- extent must start with a number
- extent may not start with 0
- extent may not contain parentheses
- extent may not be NaN
- extent must have a unit in text
- extent carrier should come first in document order
- dimensions may not be longer than 255 characters

______________________
container
______________________

- container may not be empty
- container should have @type
- container label should not be empty
- container encodinganalog should not be empty

_______________________
component
_______________________

- there may only be one unitid per component
- unittitle may not be longer than 1277 characters
- unittitle may not contain emph
- end date cannot occur before start date
- accessrestrict must have @type set to open, closed, or review 
- accessrestrict set to closed or review must have altrender
- c must have accessrestrict
- c must have @level
- names, bioghist may not contain pointers

_______________________
other observations
_______________________

- empty elements are fatal
- dsc[2] does not import
