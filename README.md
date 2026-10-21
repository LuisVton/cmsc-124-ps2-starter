# CMSC 124 Problem Set 2: Data in R

## Members

- Jemarco N. Briz — [Jmbriz123](https://github.com/Jmbriz123)
- Luis Victor V. Borbolla — [LuisVton](https://github.com/LuisVton)

## Files

- `predictions.tsv` records the value, type, length, and dimensions predicted for all 16 cases.
- `REASONING.md` explains the R rule behind each case.
- `src/analysis.R` contains the two score cleaners, roster builder, and roster summary.
- `ANALYSIS.md` compares the vector and scalar cleaners.
- `cases/`, `scripts/`, and `tests/` contain the supplied cases, runner, and public checks.

## Run the work

Use R 4.3 or newer. From the repository root, run:

```bash
./lint
./run P10
./check.sh
```

`./lint` checks the prediction table's format. `./run P10` prints one case's result. `./check.sh` runs the complete public grader and should report `76/76 checks passed`.
