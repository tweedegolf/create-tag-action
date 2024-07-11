# Create tag action

Format a deploy version tag for a git repository.

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
        shell: bash
        uses: tweedegolf/create-tag-action@main

      # ...

  # ...
```
