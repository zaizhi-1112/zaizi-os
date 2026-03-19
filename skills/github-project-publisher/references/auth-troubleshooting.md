# GitHub Auth Troubleshooting

Use this when `git push` fails during repository publishing.

## Common issues

### 1. User enters account password instead of PAT
Modern GitHub HTTPS push uses a Personal Access Token, not the account password.

### 2. 403 permission denied
Usually means:
- token lacks repo write permission
- fine-grained token is not scoped to the target repo
- user is pushing to a repo they cannot write to

### 3. HTTP2 framing error
Usually network or transport related.

Possible fix:
```bash
git config --global http.version HTTP/1.1
```

### 4. Repeated login prompts
Possible fix:
```bash
git config --global credential.helper store
```

## Minimal successful path
1. create or verify the GitHub repo exists
2. create a PAT with repository contents write access
3. push again
4. confirm the repo page renders correctly
