# Example: Structured Repo (Conventional Commits + Tags)

## Repo Assessment

> **Repo assessment:** Found 12 tags, 28/30 recent commits follow conventional format.
> Using **Structured** mode.

## Input

Git log between `v1.2.0` and `HEAD`:

```
a1b2c3d feat(auth): add OAuth2 provider support
b2c3d4e feat(api): add pagination to list endpoints
c3d4e5f fix: resolve memory leak in connection pool
d4e5f6g fix(auth): fix token refresh race condition
e5f6g7h perf: optimize database query batching
f6g7h8i docs: update API reference for v2 endpoints
g7h8i9j refactor: extract validation middleware
h8i9j0k feat!: change default response format to JSON:API
i9j0k1l chore: update dependencies
j0k1l2m ci: add automated release pipeline
k1l2m3n style: apply consistent naming to handlers
```

## Output

```markdown
## [1.3.0] - 2026-04-16

### Breaking Changes

- Change default response format to JSON:API (h8i9j0k)

### Added

- **api:** Add pagination to list endpoints (b2c3d4e)
- **auth:** Add OAuth2 provider support (a1b2c3d)

### Fixed

- Resolve memory leak in connection pool (c3d4e5f)
- **auth:** Fix token refresh race condition (d4e5f6g)

### Performance

- Optimize database query batching (e5f6g7h)

### Documentation

- Update API reference for v2 endpoints (f6g7h8i)

### Changed

- Apply consistent naming to handlers (k1l2m3n)
- Extract validation middleware (g7h8i9j)

### Build

- Add automated release pipeline (j0k1l2m)

### Other

- Update dependencies (i9j0k1l)
```

---

# Example: Freeform Repo (No Conventions, No Tags)

## Repo Assessment

> **Repo assessment:** Found 0 tags, 2/30 recent commits follow conventional format.
> Using **Freeform** mode.
>
> Freeform commits detected. I will read each commit and classify it by intent. Results may need light editing.

User chose: "last 20 commits"

## Input

```
l2m3n4o added google login button to signup page
m3n4o5p fixed the bug where users got logged out randomly
n4o5p6q WIP
o5p6q7r cleanup
p6q7r8s moved all the api routes into separate files
q7r8s9t update
r8s9t0u made the search way faster with elasticsearch
s9t0u1v updated readme with new install steps
t0u1v2w remove old payment gateway code (stripe v2)
u1v2w3x .
```

## Output

```markdown
## [1.0.0] - 2026-04-16

### Added

- Add Google login button to signup page (l2m3n4o)

### Fixed

- Fix bug where users got logged out randomly (m3n4o5p)

### Performance

- Make search faster with Elasticsearch (r8s9t0u)

### Documentation

- Update README with new install steps (s9t0u1v)

### Changed

- Move all API routes into separate files (p6q7r8s)
- Remove old payment gateway code — Stripe v2 (t0u1v2w) (?)

### Other

- Clean up (o5p6q7r)

> **Note:** 2 commits were skipped (vague messages: "WIP", "."). 1 classification is uncertain — review entries marked with (?).
> "Remove old payment gateway code" was classified as Changed, but may be a Breaking Change if the Stripe v2 API was public. Please verify.
```
