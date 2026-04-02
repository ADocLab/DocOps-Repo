# DocOps: CI/CD Pipeline

This site is deployed using:

- GitHub Actions  
- MkDocs  
- GitHub Pages  
- Automated deployment to `gh-pages` branch  
- Documentation-as-Code practices  

Whenever content is updated and pushed to the `main` branch:

1. GitHub Actions creates a fresh Ubuntu VM  
2. Installs MkDocs  
3. Builds the site  
4. Pushes the generated HTML to the `gh-pages` branch  
5. GitHub Pages updates the live site  