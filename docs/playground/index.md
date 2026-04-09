# Overview

This is the experimentation area for:

- DocOps tests  
- AI experiments  
- Code snippets  
- Workflow prototypes  

<!--This is Admonitions experimentation area-->
<!--This is markdown extentions block adding various types of admonitions to check their outputs-->

!!! info
    Indentation in markdown language is important and it tells the underlying material library that info object is called.

    !!! warning
        Any indentation issue triggers an error mechanism.

<!--Name the admonition inside the double quotes, else default name gets published -->
<!-- In MkDocs/Material, correct indentation is crucial—most rendering issues with
admonitions, tabs, and nested blocks are caused by incorrect indentation. -->

??? note "Click to expand"
    This is hidden until you click it.
    !!! example "Sample API command"
        ```bash
        curl https://example.com/api
        ```
## Deployment Flow

=== "Overview"
    High-level explanation of how documentation flows from commit to deployment.

=== "Detailed Steps"
    1. Commit pushed
    2. Workflow triggered
    3. Site built
    4. Pages updated

=== "Implementation"
    ```yaml
    - name: Build site
      run: mkdocs build
    ```

??? info "Common pitfalls"
    - Missing dependencies
    - Incorrect GitHub Pages source


