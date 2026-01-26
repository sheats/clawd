# ReturnZap

## GitHub Project Board

**URL:** https://github.com/orgs/returnzap/projects/1/views/5

**CLI Access:**
```bash
# List all items (limit 50)
gh project item-list 1 --owner returnzap --format json --limit 50

# View project metadata
gh project view 1 --owner returnzap --format json
```

**Note:** Requires `read:project` scope. If access fails:
```bash
gh auth refresh -s read:project
```

## Repo

- **Mono repo:** https://github.com/returnzap/mono
- **Issues:** `gh issue list -R returnzap/mono`
- **PRs:** `gh pr list -R returnzap/mono`
