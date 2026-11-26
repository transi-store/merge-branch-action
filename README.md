# merge-branch-action
Github action to merge translation branch on transi-store

## Usage

```yaml
- uses: transi-store/merge-branch-action@v1
  with:
    branch: ${{ github.event.pull_request.head.ref }}
    into: ${{ github.event.pull_request.base.ref }}
    api-key: ${{ secrets.TRANSI_STORE_API_KEY }}
```

`into` merges the branch into another branch instead of main, for a pull request merged into the branch of another pull request.
`main`, `master` or an empty value merge into main.
It requires `@transi-store/cli` 2.7.0 or later.
