# docs_reader

- A simple tool to track previous or nearest import lines and show helper documents automatically.

## installation

```bash
pip install docs-reader
or
pip install docs_reader
```

## usage

```python
 1. ...
 2. from doc_reader import DocsReader
 3. DocsReader()
 4. ...
 5. ...
```

## Examples:

- this tool / module help to automatically find and show the essentials documents of the given nearest import module with offline mode.

      Examples:
       1. import in your <filename>.py (e.g. main.py)
           import numpy
           import pandas as pd
           from docs_reader import DocsReader
           DocsReader()

        descriptions:
           # run the <file>.py (e.g. python main.py)
           # after that it will automatically show it's documentation.
              1. in the above 'numpy' is import that's why show it's documentation.
              2. now it show only the nearest modules documentation of pandas as: pd.

       2.  if any newline is contains before the 'from doc_reader import DocsReader', it can't be parse.
           import numpy
           import pandas as pd

           from doc_reader import DocsReader
           DocsReader()

       descriptions:
           # run the <file>.py (e.g. python main.py)
           # it will show that "could not parse the module" if newlines are contains.
