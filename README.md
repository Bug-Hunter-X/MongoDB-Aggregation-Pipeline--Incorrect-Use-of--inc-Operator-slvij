# MongoDB Aggregation Pipeline Bug: Incorrect $inc Usage

This repository demonstrates a common error when using the `$inc` operator within a MongoDB aggregation pipeline.  The `$inc` operator is designed to increment a field *within a document*, not to modify the results of the aggregation pipeline after it has completed. Attempting to use it at the end of the pipeline, as shown in `bug.js`, results in an error or unexpected behavior.

The solution (`bugSolution.js`) demonstrates the correct way to increment the count, which involves either performing the increment during the aggregation pipeline (using $sum) or updating the documents directly after aggregation.

## How to Reproduce

1. Clone this repository.
2. Run `bug.js` to observe the incorrect behavior.
3. Run `bugSolution.js` to see the corrected approach.
