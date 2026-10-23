# Corpus Schema
entry content in Yaml (yet another markup language) format
see [corpus-example.yaml](https://eidolon-7.github.io/ai-corpus/corpus/meta/corpus-example.yaml) for example
Each entry contains the following top-level containers, described below:
- metadata 
- references 
- content

## version
1.0

## history of schema
2026/10/23 - v1.0

# metadata
contains value-added descriptions of the entry.
top-level container for metadata for the entry. Peer of references and content containers.

## id
string value representing a sequential identifier
J for journal entry, C for corpus entry

## itemid
string value representing a longer unique entry name. 
Usually consists of a date in yyyymmdd format appended with the title as dash or underscore separated words. 
Does not include the .yaml extension.
e.g. 20261023-corpus-schema

## title
short description of the entry

## type
type category of the entry. Choose one of the following:
- reflection
- argument
- principle
- axiom
- question
- hypothesis
- observation
- dialogue
- evaluation
- specification
- proposal
- definition
- narrative
- artifact
- meta

## schema_version
version of the yaml schema format. This document represents the latest version description.
 
## authorship
human/AI contributors to entries.

### primary
primary contributor to the entry. Singular item with the fields below:

#### id
name/handle of the contributor.

#### type
contributor type:
- human 
- ai-llm

#### model
AI (LLM) model, e.g. GPT 5 Thinking mini.  Humans only have the one model, so omitted.

#### role
type of contribution:
- author 
- editor 
- compiler 
- curator 
- translator 
- reviewer

### contributors
list of contributors with the same fields as the primary contributor

## history
list of historical versions.  Each history item contains the fields below.

### version
version/revision number of the entry. Broken into major/minor version numbers as in software development.

### date
date that the version/revision was created.

### status
historical status of the revision.  
- draft 
- active 
- superseded 
- withdrawn 
- archived 
- experimental

### changes
list of changes, described in human-readable descriptions

## provenance
documented history of ownership of the entry

### sources
list of sources to reference entries

#### type
type of source
- navigation - navigation to index of entries
- entry - entry itself in the canonical location

#### url
url of the provenance source in the canonical location

# references
list of external sources used to create the entry.

## type
type of the reference - implies the usage of the source.  
Acts as the root of the individual reference in version 1.0.
list of reference types is in development.
- entry
- article
- book
- video-game
- theory

### relationship
- research
- expansion
- inspiration
- clarification

### name
short description of the reference

### url
internet location of an online reference

### isbn
book identifier for a literary reference

# content
main content. schema of content container is for future development in version 1.0

## keywords
Jagged array of non-canonical keywords in the entry

## topic
short description of the topic of the content

## summary
paragraph summary of the entry