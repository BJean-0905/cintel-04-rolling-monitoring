# Continuous Intelligence

This site provides documentation for this project.
Use the navigation to explore module-specific materials.

## How-To Guide

Many instructions are common to all our projects.

See
[⭐ **Workflow: Apply Example**](https://denisecase.github.io/pro-analytics-02/workflow-b-apply-example-project/)
to get these projects running on your machine.

## Project Documentation Pages (docs/)

- **Home** - this documentation landing page
- **Project Instructions** - instructions specific to this module
- **Your Files** - how to copy the example and create your version
- **Glossary** - project terms and concepts

## Additional Resources

- [Suggested Datasets](https://denisecase.github.io/pro-analytics-02/reference/datasets/cintel/)

Rolling_Monitoring

## Dataset

For this dataset, I used the provided data, rolling_metrics_timeseries.
Dataset includes Timestamp, requests, errors and latency in ms.

## Signals

Signals include a rolling window which I adjusted from 3 to 4. Rolling mean for requests and errors were already added. I added standard deviation for both the requests and errors. Additionally, I changed the output for errors and requests to round to whole numbers.

## Experiments

I experimented with standard deviation to see if the rolling windows affected standard deviation and what returns may occur with a dataset that had larger numbers like the request column vs. lower numbers like the error column.

## Results

Standard deviation provided interesting results with the requests column, larger numbers. Results were limited with the error column which had lower numbers, returs were 1-2. I also noticed that in rounding, the standard deviation calculations may be off. For example, 8 errors with a rolling mean of 5, standard deviation 2. Mathmatically appears incorrect.

## Interpretation

Take in to account the value of standard deviation on larger numbers while being mindful of smaller data sets with lower numbers. Rounding is visually helpful in analyzing returns but may cause slight inaccuracies.
