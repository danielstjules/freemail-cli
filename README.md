# freemail-cli

```
Filters or selects free/personal/disposable email addresses

Usage
  $ freemail-cli [options] <file>

Matches both free and disposable emails by default.

Options
  -d, --disposable  Only match disposable emails
  -f, --free        Only match free emails
  -i, --inverse     Print emails that don't match

Examples
  $ freemail-cli ./path/to/file
  $ cat ./path/to/file | freemail-cli
```

#### Installation

```
npm install -g freemail-cli
```
