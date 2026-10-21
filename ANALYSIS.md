# Vector and Scalar Evaluation

In `clean_scores_vector()`, I begin by converting the supplied scores to doubles while restoring their names with `setNames(as.double(scores), names(scores))`. The next three operations work across the entire vector, not by visiting one student at a time. First, the logical mask `is.na(out)` identifies every missing score and subassignment replaces those positions with zero. Next, `out * 2` doubles every element. Finally, the comparison `out > 20` creates another logical mask, and subassignment caps all marked values at 20.

For the sample scores, Ada's 8 becomes 16, Grace's missing value becomes 0, Linus's 12 becomes 24 and is capped at 20, and Barbara's 4 becomes 8. Grace is not handled by a special iteration: her position participates in the same whole-vector expressions as the others. Replacing missing values before multiplication is important because doubling `NA` would otherwise leave it missing.

The vector approach expresses the transformation as a small sequence of operations. It avoids manually tracking an index and makes it easier to check that the same rules apply to every score. I would generally keep this version in an R program because it is concise and communicates the intended transformation clearly.





Replace this paragraph after your checks pass. Trace one input, including the
missing value, through `clean_scores_vector()` and `clean_scores_scalar()`.
Compare the two evaluation models, identify where recycling would change the
answer, and explain which implementation you would keep in an R program.
