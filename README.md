# ArchivesSpace Technical Advisory Council
## Metadata Standards Sub-Team

### Example Encoded Archival Description (EAD) Documents

Within this repository, members of the Metadata Standards Sub-Team track
examples of [EAD Documents](https://www.loc.gov/ead/) used for 
testing importation and the extraction of metadata within ArchivesSpace.

The repository also includes a number of dedicated test files.

For a node-by-node accounting of the import mapping, use the [TACmetadata_test_import.xml](https://github.com/ASpace-Metadata-Standards/ead-examples/blob/master/test_files/TACmetadata_test_import.xml) file, which shows the XPath of the imported node.

### EAD2002 Import Gotchas
  
______________________
resource-level
______________________
- extent is required
- extent has to start with a number
- unitdate is required
- unitid is required
- unitid is limited to 50 characters
- unittitle is limited to 255 characters

___________________
extent and physdesc
______________________

- physdesc should have @altrender 
- extent may not contain commas
- extent should have @altrender denoting "whole" or "part"
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
dao
_______________________
- xlink:title is required
- xlink:show is required (use as a mule to get in file_version)
- xlink:href is required

_______________________
component
_______________________

- unittitle may not be longer than 1277 characters
- unittitle may not contain emph
- end date cannot occur before start date
- unitdate cannot be invalid
- unitdate is limited to 255 characters
- accessrestrict must have @type set to open, closed, or review 
- accessrestrict set to closed or review must have altrender
- c must have accessrestrict
- c must have @level
- names, bioghist may not contain pointers
- must have one or both of unittitle, unitdate

_______________________
other observations
_______________________

- empty or head-only note elements are fatal
- dsc[2] does not import
- empty children of controlaccess are fatal
