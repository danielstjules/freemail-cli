# freemail-cli

```
Filters or selects free and disposable email addresses

Usage
  $ freemail-cli [options] <file>

Matches free emails, including disposable, by default

Options
  -d, --disposable  Only match disposable emails
  -i, --inverse     Print emails that don't match

Examples
  $ freemail-cli ./path/to/file
  $ cat ./path/to/file | freemail-cli
```

#### Overview

Free emails include gmail.com, yahoo.com, and all those listed in [this file](https://github.com/willwhite/freemail/blob/master/data/free.txt). Disposable emails include mailinator.com, guerillamail.com, and [all others here](https://github.com/willwhite/freemail/blob/master/data/disposable.txt).

```bash
$ cat emails.csv
foo@gmail.com
bar@mailinator.com
baz@zendesk.com

# Free emails
$ cat emails.csv | freemail-cli
foo@gmail.com
bar@mailinator.com

# Non-free (e.g. work, company)
$ cat emails.csv | freemail-cli -i
baz@zendesk.com

# Disposable
$ cat ~/emails.csv | freemail-cli -d
bar@mailinator.com

# Non-disposable
$ cat ~/emails.csv | freemail-cli -di
foo@gmail.com
baz@zendesk.com
```

#### Installation

```
npm install -g freemail-cli
```
