# Reasoning Before Execution

Write the rule behind each case before you commit your predictions. Replace
every placeholder line below with one to three sentences that name the rule
producing that case's value, type, length, and dimensions. One rule is enough.
After you run and find a miss, add a short correction entry under that case in a
later commit.

## P01
Atomic vectors share one storage type. The double `3.5` is highest on the logical–integer–double ladder, so `TRUE` becomes 1 and `2L` becomes 2; the three values form an undimensioned double vector.

## P02
A character value makes the entire atomic vector character, converting `1L` to `"1"` and `TRUE` to `"TRUE"`. The result has three strings and no `dim` attribute.

## P03
Addition works element by element and recycles the two integer addends as 1, 2, 1, 2. Integer plus integer remains integer here, giving four values without dimensions.

## P04
Positive positions 3 and 1 select `third` then `first`, retaining both their names and integer storage. Indexing returns a two-element vector with no dimensions.

## P05
A negative index removes position 2, leaving the first and third integers in order. The result has length two and no dimensions.

## P06
`is.na(x)` is TRUE for the missing integer, while `x > 10L` is TRUE for 12; elementwise OR selects both. `TRUE | NA` is TRUE, so the missing element is retained as an integer NA, yielding length two and no dimensions.

## P07
A factor displays level labels but stores integer codes, and its explicit levels stay ordered `low`, `high`. Its three observations have `typeof` integer, length three, and no dimensions.

## P08
A list keeps its two unlike members separate: a two-element integer vector and a one-element character vector. `typeof` is list, and `length` counts its two top-level entries; it has no dimensions.

## P09
A data frame is a list of columns, so `typeof()` is list and `length()` counts its two columns. The `id` column holds integers 1 and 2, while `passed` holds TRUE and FALSE; two rows and two columns give it dimensions 2x2.

## P10
R fills the integer matrix down its columns, then recycles 10 and 20 across its stored values. The sums are 11, 22, 13, 24, 15, and 26 in storage order; integer addition keeps integer type, length six, and dimensions 2x3.

## P11
Without `na.rm = TRUE`, the missing value makes the mean missing. `mean()` returns one double value with no dimensions.

## P12
With `na.rm = TRUE`, `mean()` drops the missing value and averages 8 and 10 to get 9. The result is one double value with no dimensions.

## P13
`1:3` first makes an integer vector, but assigning the double 2.5 widens the whole vector to double. The values are 1, 2.5, and 3, with length three and no dimensions.

## P14
`ifelse()` replaces the missing score with 0 and doubles the other scores, giving 14, 0, 24, and 8. Subassignment caps 24 at 15, leaving a double vector of length four with no dimensions.

## P15
`array()` keeps the eight integers from `1:8` in storage order and adds a dimension attribute of 2x2x2. Its `typeof()` is integer and its length is eight, even though it has three dimensions.

## P16
Index 0 selects no elements from the integer vector. The result is an empty integer vector of length zero with no dimensions.
