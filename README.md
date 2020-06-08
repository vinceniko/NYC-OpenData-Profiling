# NYC Open Data Profiling

The final project for Big Data. Our group had to use Spark to profile (derive column metadata--data types and semantic types) for ~2k datasets from NYC's Open Data initiative.

## Repo Info

`5-Project-Open Data Profiling, Quality, and Analysis.pdf` contains the assignment instructions. `Biggest Data Report.pdf` contains the final group report.

## My Role

I wrote a custom reducer in `basic_metadata.py` which was used to derive all the datatype metadata for Part 1. I wrote all of the code and much of the report for Part 2. I also wrote the timing code found in `timing.py`.

## Running

This was written for internal usage but I'm keeping it in the README for reference.

### Timing

Use timing module to automate timing of a function that operates on a series of dfs.
`timing.timed` accepts a closure. Refer to `sample.py` for a good example of how to use timing.timed with a closure.

### From CLI

typical usage: `./env.sh "<file.py> <ds dir> <number of ds (limit)> <random order>"`
Limit and Rand are optional. Use `-` to not pass arg.
example: `./env.sh "sample.py datasets - True"`

refer to `cli.py` for an explanation of how to grab arguments from the cli

Run as ./env.sh "basic_metadata.py /user/hm74/NYCOpenData 30 print"
