# semantic-release-action

## How to use

```
jobs:
  release:
    needs: beforebuildtest
    if: github.event_name == 'push'
    runs-on: ubuntu-latest

    steps:
      - name: Check-out
        uses: actions/checkout@v3
        with:
          fetch-depth: 0

      - name: Semantic release
        uses: wintero92/semantic-release-action@v1
        with:
          GH_TOKEN: ${{secrets.GH_TOKEN}}
```

## Inputs

See `action.yaml` for possible inputs.