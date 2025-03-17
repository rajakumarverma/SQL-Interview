# Functions and Syntax for Looking Up Values Across Different Tables and Sheets

## 1. VLOOKUP Syntax:

```excel
=VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])
```
## 2. INDEX + MATCH Syntax:
```excel
=INDEX(return_range, MATCH(lookup_value, lookup_range, 0))
```
## 3. XLOOKUP Syntax (for newer Excel versions):
```excel
=XLOOKUP(lookup_value, lookup_array, return_array, [if_not_found], [match_mode], [search_mode])
