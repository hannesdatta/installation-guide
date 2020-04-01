# Downloading files from Dropbox

Raw data files are ideally hosted on a secure server; in practice, many researchers
store their data on Dropbox, though (e.g., because they want to enable
co-authors *not* used to reproducible workflows to also access these
files.

A good way then is to *host* your raw data files in a Dropbox folder. Thereby,
- your co-authors have access to the files (and, e.g., can populate
  the directories with their own data collections)
- you can still programmatically access these files and reproduce
  them to any directory on your hard disk.

Data structures for projects typically are:

```
\root\code\analysis   - Your analysis
\root\code\derived    - Your data preparation
\root\data\
           dataset1    - A dataset
           dataset2    - Another dataset
```

...while the raw data actually sits somewhere on Dropbox.

Here is a Python script that *downloads* the data to your
local directory structure.

<script src="https://gist.github.com/hannesdatta/10422a6fbb584f245c83361245335741.js"></script>
