# fixit example

```
# clone repository
git clone git@github.com:chdsbd/fixit-example.git && cd fixit-example

# install fixit
poetry install

# run fixit
poetry run python3 -m fixit.cli.run_rules

# verify error
```

Running fixit returns the following output. There is an unexplained exception, a mention of running pyre, and a flake8 error.

```
poetry run python3 -m fixit.cli.run_rules
Scanning 1 files
Testing 21 rules

Encountered exception <class 'Exception'> for the following paths:
./main.py
Running `pyre start` may solve the issue.
main.py:4:1
    E305: expected 2 blank lines after class or function definition, found 1

Found 1 reports in 1 files in 0.33 seconds.
```
