This file will eventually include every node pair allowed in EAD2002 with the exception of 
- eadgrp
- archdescgrp
- dscgrp 
i.e. the super-wrappers around multiple descriptions. 

The following attributes were omitted:
- @entityref

as well as the following on linking elements:
- @linktype (silently corrected to xlink:type)
- @actuate (silently corrected to xlink:actuate)
- @arcrole (silently corrected to xlink:arcrole)
- @show (silently corrected to xlink:show)
- @role (silently corrected to xlink:role)
- @title (silently corrected to xlink:title)
- @href (silently corrected to xlink:href)
- @label (silently corrected to xlink:label)

The content of non-empty nodes is their XPath unless the value is type-controlled.
