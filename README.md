# Library Catalog Parser

A simple JavaScript project that parses raw catalog card strings into structured book objects.

## Features

- Converts raw string data into JavaScript objects
- Cleans extra spaces using `trim()`
- Handles missing values with `"Unknown"`
- Converts valid years into numbers using `parseInt()`

## Example Raw Data

```javascript
"From a Buick 8 | King, Stephen | 2002 | Shelf K7"
Parsed Output
{
  title: "From a Buick 8",
  author: "King, Stephen",
  year: 2002,
  location: "Shelf K7"
}
Functions
parseCard(rawString)

Parses a single catalog card string into an object.

parseCatalog(rawCards)

Loops through all raw catalog cards and stores parsed objects inside a catalog array.

Example Usage
const catalog = parseCatalog(rawCatalogCards);

console.log(catalog);
console.log(catalog.length);
Technologies Used
JavaScript
Arrays
Objects
Loops
String methods

```text
Build library catalog parser with object conversion