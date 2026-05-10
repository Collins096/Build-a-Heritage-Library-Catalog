# Heritage Library Catalog

A JavaScript project that parses, validates, searches, groups, and exports library catalog records.

## Features

- Parse raw catalog card strings into structured objects
- Handle missing data with fallback values
- Search books by author
- Group books by decade
- Render formatted library cards
- Validate catalog entries
- Export catalog data to JSON
- Export catalog data to CSV
- Generate summary statistics

---

## Technologies Used

- JavaScript
- Arrays
- Objects
- Loops
- String methods
- JSON methods

---

## Project Structure

### Raw Catalog Data

The project starts with an array of raw catalog strings:

```javascript
"From a Buick 8 | King, Stephen | 2002 | Shelf K7"
```

---

## Functions

### parseCard(rawString)

Converts a raw catalog string into an object.

#### Example Output

```javascript
{
  title: "Dune",
  author: "Herbert, Frank",
  year: 1965,
  location: "Shelf H3"
}
```

---

### parseCatalog(rawCards)

Loops through all raw catalog cards and converts them into structured objects.

---

### findByAuthor(catalog, author)

Searches the catalog for books whose author contains the search term.

#### Example

```javascript
const kingBooks = findByAuthor(catalog, "king");
```

---

### groupByDecade(catalog)

Groups books into decade categories.

#### Example Output

```javascript
{
  "1950s": [...],
  "1960s": [...],
  "1980s": [...]
}
```

---

### renderEntry(entry)

Formats a catalog entry as a printable library card.

#### Example Output

```text
-------------------------
Title: Dune
Author: Herbert, Frank
Year: 1965
Location: Shelf H3
-------------------------
```

---

### validateEntry(entry)

Checks whether an entry contains valid values for:
- title
- author
- year
- location

Returns:
- `true` if valid
- `false` if invalid

---

### exportToJSON(catalog)

Converts the catalog into formatted JSON.

#### Example

```javascript
console.log(exportToJSON(catalog));
```

---

### exportToCSV(catalog)

Converts the catalog into CSV format.

#### Example Output

```csv
Title,Author,Year,Location
"Dune","Herbert, Frank",1965,"Shelf H3"
```

---

## Summary Statistics

The project also calculates:

- Total number of books
- Total decade groups
- Oldest published book
- Newest published book

---

## Example Usage

```javascript
const catalog = parseCatalog(rawCatalogCards);

console.log(catalog.length);

const kingBooks = findByAuthor(catalog, "king");

console.log(kingBooks);

const byDecade = groupByDecade(catalog);

console.log(byDecade);
```

---

## Learning Concepts

This project practices:

- Functions
- Arrays
- Objects
- Loops
- Conditionals
- Template literals
- String manipulation
- JSON handling
- CSV formatting
- Data validation

---

## Author

Collins Mwangi