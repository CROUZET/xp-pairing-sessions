# Bookstore's Stock Replenishment

Your friend Maxime has a bookstore.

Every month he do a full inventory of the shop, then order books to replenish the stock. Which takes him several hours...

As you are tired of hearing him complain about how thankless this task is, you have decided to give him a helping *developer* hand.

## Your task

is to provide a function that returns the list of books and the quantity to order

In inputs, you'll have:
- the catalog: list of books you want to replenish, with le desired amount limit
- the inventory notes: list of notes Maxime has writen during the inventory

## Exemple

With the catalog:
- "The Great Gatsby" 10
- "White Fang" 10

And the inventory notes:
- "The Great Gatsby"
- "The Great Gatsby"
- "White Fang"
- "The Great Gatsby"

Then, the replenish list must be:
- "The Great Gatsby" 7
- "White Fang" 9

## Notes Rules

Be carful that Maxime may use different form for the notes:
- the exact book name: "The Great Gatsby"
- one of the principal keyword: "Gatsby" (uniq in the catalog)
- the complete acronym of the book: "tgg" (uniq in the catalog)

He can also stack books in a same note, using " x<number>" suffix
- "The Great Gatsby x4"
- "tgg x10"

The case do not matter
- "The Great Gatsby"
- "the gReat Gatsby"
- "TGg"

The notes may include books no longer in the catalog

## Replenish List Rules

- The list only include books from the catalog
- The list only include books that need to be replenish
