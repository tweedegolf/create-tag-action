# Create tag action

Format a deploy version tag for a git repository.

The generated tag has the exact format `<unix-timestamp>-<7-char-commit-sha>`.
Example: `1713187200-1a2b3c4`

## Usage

The tag is exposed both as a step output (`steps.<id>.outputs.tag`) and as an
environment variable (`env.tag`). Prefer the step output — it is statically
declared in `action.yml`, so editor tooling and workflow linters can resolve it.

```yaml
jobs:
  docker:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - name: Create tag
        id: tag
        uses: tweedegolf/create-tag-action@main

      - name: Use the tag
        run: echo "Tag is ${{ steps.tag.outputs.tag }}"
```
