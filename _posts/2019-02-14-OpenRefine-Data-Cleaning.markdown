---
layout: post
title:  "Data-lit: Collections(1.5) OpenRefine Data Cleaning"
date:   2019-02-14 12:49:44 -0800
categories: data lit
---
Today I cleaned up a large dataset of items belonging to the Powerhouse Museum in
Australia. We used a popular open-source data cleaning tool made by Google, OpenRefine.

It felt easier to clean than "Metamorphosis". I think the reason why is because
it was an analytic record rather than just text. The OpenRefine user interface felt
really good and easy to use.

We used a numeric facet-(break up the data into specific characteristics) to find
non-numeric values and removed all rows which didn't have a number in the Record
Id column.

To detect duplicates we used a unique identifier which in this case was the Record
Id. We used blank down which leaves the first instance of a duplicate intact and
turns the rest of the duplicates blank. We then used another facet(text facet) to
remove all blank cells.

Right next to the facets tab, OpenRefine has a tab to undo it has a history of past
actions.

**Fix Categories Attribute**  
  Categories column has multiple categories separated by a pipe(\|) character
- We split by the pipe(\|) into their own cell(atomization)
- We went from 41895 to 93181 rows (We will merge back later)
- Due to small inconsistencies like capitalization, misspelling, or whitespaces
there are more columns than we need, luckily OpenRefine has clustering
- Rejoin by /|(pipe char.)
- We use GREL (General Refine Expression Language) value.split('\|').uniques().join('\|')

**Export**
- Last step is to export file in the same format we imported it(tsv)

**Review**
- The first step in any data science project is cleaning the data
- Handle missing data, inconsistencies, and duplicate records
- Faceting: break your data into smaller buckets that are easy to work with
- Atomization: splitting multi-value cells into separate cells
- Clustering: a technique which groups similar data
