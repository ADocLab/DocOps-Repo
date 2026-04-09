# Overview
This file is ground for learning some advanced material types and their uses.

# Tabs
To use tabs in mkdocs, you must add the following markdown extensions:

```
markdown_extensions:
  - pymdownx.superfences
  - pymdownx.tabbed
```
# Syntax
Prefix '===' to a string to add a tab.


# Example 1:
=== "High-level Flow"
    Documentation is built automatically using CI/CD pipelines and deployed without manual steps.

=== "Developer View"
    Developers push Markdown changes to `main`, triggering a GitHub Actions workflow.

=== "System View"
    A fresh VM builds the site and deploys HTML output to the `gh-pages` branch.

# Example 2: 
=== "YAML"
    ```yaml
    on:
      push:
        branches:
          - main
    ```

=== "Bash"
    ```bash
    git push origin main
    ```

=== "Explanation"
    This workflow starts on every push to the main branch.

# Use of ``

    Use `` `code` `` syntax

# Expandable Section   

??? info "Why this design was chosen"
    This architecture allows us to scale documentation across teams
    without manual deployments

# Admonitions as Architectural Signals

!!! note "Architecture decision"
    Documentation is deployed via CI/CD to ensure consistency
    and eliminate manual errors.

# Tables for Structured Information

| Component | Responsibility |
|---------|----------------|
| MkDocs | Site generation |
| GitHub Actions | CI/CD |
| GitHub Pages | Hosting |

