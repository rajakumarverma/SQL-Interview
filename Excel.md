# Functions and Syntax for Looking Up Values Across Different Tables and Sheets
## 1. VLOOKUP Syntax:
excel
Copy
=VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])
lookup_value: The value to search for.
table_array: The range of data to search in.
col_index_num: The column number in the table from which to retrieve the value.
[range_lookup]: Optional. Use TRUE for an approximate match, or FALSE for an exact match.
2. INDEX + MATCH Syntax:
excel
Copy
=INDEX(return_range, MATCH(lookup_value, lookup_range, 0))
return_range: The range to return the value from.
lookup_value: The value to search for.
lookup_range: The range to search for the lookup value.
0: For exact match.
3. XLOOKUP Syntax (for newer Excel versions):
excel
Copy
=XLOOKUP(lookup_value, lookup_array, return_array, [if_not_found], [match_mode], [search_mode])
lookup_value: The value to search for.
lookup_array: The range where you want to find the lookup_value.
return_array: The range from which to return the result.
[if_not_found]: Optional. The value to return if lookup_value is not found.
[match_mode]: Optional. Specifies the match type (0 for exact match).
[search_mode]: Optional. Specifies the search mode (1 for searching from first to last, -1 for reverse).
