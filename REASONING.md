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
Replace this line with the rule that decides this case.

## P10
Replace this line with the rule that decides this case.

## P11
Replace this line with the rule that decides this case.

## P12
Replace this line with the rule that decides this case.

## P13
Replace this line with the rule that decides this case.

## P14
Replace this line with the rule that decides this case.

## P15
Replace this line with the rule that decides this case.

## P16
Replace this line with the rule that decides this case.
