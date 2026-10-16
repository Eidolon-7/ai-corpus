# Corpus Schema
Yaml (yet another markup language) - entry content

# id
string value representing a sequential identifier
J for journal entry, C for corpus entry
root element for yaml

## itemid
string value representing a longer unique entry name

## metadata
container for metadata for the entry

### author
human/AI contributors to entries

### title
human-readable string representing the title of the entry

### created_by
content writer/contributor/editor

### created_on
initial creation date

### updated_on
last updated date

### version
current version of the entry formatted as a software-development lifecycle version number
Major/minor versions

### status
draft

### canonical_location:
Location the corpus is stored
GitHub repo

### keywords
Jagged array of non-canonical keywords in the entry

### topic

### references
other corpus entries or internet urls

### summary
paragraph summary of the entry