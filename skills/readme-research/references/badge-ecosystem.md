# Badge Ecosystem Reference

Comprehensive guide to GitHub README badges, their sources, and psychological signals.

## Badge Categories

### Build Status
**Signal:** "The code compiles and passes tests right now."

| Badge | Source | Example |
|-------|--------|---------|
| Build Passing | GitHub Actions | ![Build](https://img.shields.io/github/actions/workflow/status/user/repo/ci.yml) |
| CI Status | CircleCI, Travis | ![CircleCI](https://img.shields.io/circleci/build/github/user/repo) |

**When to use:** Always. This is table stakes for any serious project.

### Code Quality
**Signal:** "The maintainers care about long-term stability and testing."

| Badge | Source | What it Shows |
|-------|--------|---------------|
| Code Coverage | Codecov, Coveralls | Test coverage percentage |
| Code Quality | SonarCloud, CodeClimate | Maintainability grade |
| Type Coverage | TypeScript, mypy | Type safety percentage |

**When to use:** If you have meaningful coverage (>60%). Don't badge 15% coverage.

### Package/Version
**Signal:** "This is a releasable product, not just a script."

| Badge | Source | Example |
|-------|--------|---------|
| npm version | npm | ![npm](https://img.shields.io/npm/v/package-name) |
| PyPI version | PyPI | ![PyPI](https://img.shields.io/pypi/v/package-name) |
| Crates.io | Cargo | ![Crates.io](https://img.shields.io/crates/v/package-name) |
| Maven | Maven Central | ![Maven](https://img.shields.io/maven-central/v/group/artifact) |

**When to use:** If published to a package registry.

### Social Proof
**Signal:** "The crowd has vetted this; I am not the first user."

| Badge | Source | What it Shows |
|-------|--------|---------------|
| GitHub Stars | GitHub | Community endorsement |
| Downloads | npm, PyPI | Usage volume |
| Contributors | GitHub | Community involvement |
| Forks | GitHub | Developer interest |

**When to use:** If numbers are meaningful. 5 stars doesn't impress; 5000 does.

### License
**Signal:** "I can legally use this in my corporate/personal project."

| Badge | Type | Corporate-Friendly |
|-------|------|-------------------|
| MIT | Permissive | Yes |
| Apache 2.0 | Permissive | Yes |
| BSD | Permissive | Yes |
| GPL | Copyleft | Caution |
| AGPL | Strong Copyleft | Often blocked |

**When to use:** Always. Corporate developers filter by license first.

### Activity
**Signal:** "This project is alive and will be supported."

| Badge | Source | What it Shows |
|-------|--------|---------------|
| Last Commit | GitHub | Recent activity |
| Release Date | GitHub | Latest release |
| Maintenance | Custom | Active/Passive/Seeking |

**When to use:** If actively maintained. Don't badge if last commit was 2 years ago.

## Badge Styling

### Consistent Styles

Use ONE style across all badges:

| Style | Look | Best For |
|-------|------|----------|
| `flat` | Modern, clean | Most projects |
| `flat-square` | Sharp edges | Technical projects |
| `plastic` | 3D gradient | Legacy look |
| `for-the-badge` | Large, bold | Hero sections |

**Example with consistent style:**
```markdown
![Build](https://img.shields.io/github/actions/workflow/status/user/repo/ci.yml?style=flat-square)
![Coverage](https://img.shields.io/codecov/c/github/user/repo?style=flat-square)
![npm](https://img.shields.io/npm/v/package?style=flat-square)
```

### Custom Badges

Use Shields.io for custom metrics:
```
https://img.shields.io/badge/[LABEL]-[MESSAGE]-[COLOR]?style=flat-square
```

Examples:
- `https://img.shields.io/badge/docs-passing-green`
- `https://img.shields.io/badge/PRs-welcome-brightgreen`
- `https://img.shields.io/badge/made%20with-love-red`

## Badge Anti-Patterns

### Badge Overload
**Problem:** 15+ badges creating visual chaos.
**Fix:** Limit to 5-7 most important badges.

### Inconsistent Styling
**Problem:** Mix of flat, plastic, for-the-badge styles.
**Fix:** Pick one style, use it everywhere.

### Vanity Badges
**Problem:** "Made with JavaScript" - adds no value.
**Fix:** Only badge things that inform decisions.

### Stale Badges
**Problem:** Coverage badge showing 0% from broken CI.
**Fix:** Ensure all badge sources are working.

### Meaningless Numbers
**Problem:** Badging 3 stars, 12 downloads.
**Fix:** Only badge impressive numbers.

## Recommended Badge Sets

### Minimal (3-4 badges)
```
[Build Status] [Version] [License]
```

### Standard (5-6 badges)
```
[Build Status] [Coverage] [Version] [Downloads] [License]
```

### Comprehensive (7 badges max)
```
[Build Status] [Coverage] [Quality] [Version] [Downloads] [License] [Last Commit]
```

## Badge Placement

**Hero Section:** Primary badges (build, version, license)
**After Description:** Secondary badges (downloads, stars)
**In Tables:** For comparing features across versions

## Dynamic Badges

For real-time data, use:
- Shields.io dynamic badges
- GitHub Actions to update badge data
- Custom endpoints returning badge JSON

Example dynamic endpoint:
```json
{
  "schemaVersion": 1,
  "label": "active users",
  "message": "1,234",
  "color": "green"
}
```
