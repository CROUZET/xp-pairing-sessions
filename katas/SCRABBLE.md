# SCRABBLE 🅰️🅾️🅱️🅿️️ℹ️♏️❎

## Goal

Given a maximum of 7 letters, you must return the best words to play

## Definition of "best words to play"

- Length: the word must as close as possible to the provided letters
- Scoring: the higher letters' score value the best

## Parameters

- "letters": a string of max 7 characters
- "limit": the number of suggestions to return

## Example

```ruby
suggest(letters: "NCETABI")
# => "CABINET"

suggest(letters: "ABCDEFG")
# => "ACIDIFIABLE" # to confirm :) 
```

## What's provided

- The list of words in the french dictionary can be found here: https://www.pallier.org/liste-de-mots-francais.html

## Constraints

- words with dashes are NOT accepted

## Ideas to go further

- Handle multiple suggestions
- Languages: handle dictionaries in other languages and specific letter scoring
- Jocker: handle the presence of jokers "_" in the letters (2 max)
- ...
