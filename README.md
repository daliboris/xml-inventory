# Xml Inventory

Xml Inventory is application for XML files content analysis and creating interactive summary reports.

## Existing applications

### FreqX

- developed by Liam Quin
- <https://gitlab.com/barefootliam/freqx>
- main features
  - scans
    - a single XML file
    - XML files in given folder (and subfolders)
    - files defined in XML file
  - supports catalogs
  - report on frequencies of
    - element names
    - element parent names
    - attribute names
    - attribute element names
    - attribute values
  - reports not well-formed files
  - reports in
    - XML
    - HTML (with bar graphs)
    - CSV
  - programming language: XSLT 3.0

### NormaTEI

- developed by Pierpaolo Sichera
- <https://github.com/pierpaolosichera/NormaTEI> (source code not available)
- main features
  - scans files in given folder
- report on frequencies of
  - element names and values
  - attribute names and values
  - XPaths (matches) and unique XPaths
- report as table with advanced filters and summarization
- export to
  - CSV
  - Excel
- programming framework: [4D](https://www.4d.com/)

### BaseX

- developed by team BaseX
- <https://github.com/BaseXdb/basex>
- main features
  - scans files in the database
- report on frequencies of
  - element names
  - attribute names and values, minimum and maximum values for numbers
  - attribute values
  - XPaths
  - text content (separate words)
  - namespaces and prefixes (without frequency)
- reports
  - list in plain text
  - graphs (for attributes)
- programming language: Java

## Xml Report Expectations

- analysis of
  - one file
  - files in one folder
  - files in one folder and subfolders
  - defined files (using wildcards or regex expressions)
- XML catalogs support
- analysis settings
  - start element (not starting from the root element)
  - number of stored values (0, first N [absolute or %], all)
- report on
  - not well-formed files
  - number of analyzed files and folders
  - depth of folder structure
  - elements + used namespace and prefix, parent element, XPath, unique XPaths, if is root element
  - attributes + used namespace and prefix, parent element, XPath, unique XPaths, values
  - processing instructions
  - comments
  - entities + parent element or attribute
  - text content of elements
  - characters in
    - element and attribute names
    - text content
- different views of data
  - unique elements (with number of occurrences)
    - with list of attributes, parent and child elements
  - unique XPath for each element
- report can have
  - hierarchical structure
  - flat structure
  - graphs
- names, frequencies and content are searchable and sortable
- user can go to concrete place in containing document
- export to
  - XML
  - CSV
  - HTML
  - PDF (?)
  - Markdown (?)

## Xml Inventory Plans

- fast and scalable portable desktop application (Windows, macOS, Linux)
- parallel file analysis processing
- considered programming languages and frameworks
  - [.NET 10](https://dotnet.microsoft.com/en-us/download/dotnet/10.0)
  - [C#](https://learn.microsoft.com/en-us/dotnet/csharp/) (combined with [F#](https://learn.microsoft.com/en-us/dotnet/fsharp/)?)
  - [Avalonia](https://github.com/AvaloniaUI/Avalonia)

## Use cases

### TEI ODD

- list unique elements if the collection of TEI files
- prepare TEI ODD only with available elements
