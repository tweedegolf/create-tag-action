# Create tag action

Format a deploy version tag for a git repository.

The generated tag has the exact format `<unix-timestamp>-<7-char-commit-sha>`.
Example: `1713187200-1a2b3c4`

## Usage

```
# ...
jobs:

  # ...

  docker:
    runs-on: ubuntu-latest
    steps:
      # ...
      - uses: actions/checkout@v4

      - name: Create tag
        uses: tweedegolf/create-tag-action@main

      # ...

  # ...
```
