# Setup MK Docs
A static web-site using github pages

## Install
If you need to add Python, as I do on Alpine, run:
```
doas apk add python2 py3-pip
```
Follow the install instructions  
https://squidfunk.github.io/mkdocs-material/getting-started/   
  
create a new project folder and install, run it.  
```
mkdocs new docs
cd docs
mkdocs serve
```

To build the HTML pages run:
```
mkdocs build
```
Which creates a site/ folder of the HTML project.   

For custom index ordering in mkdocs use a community plugin.  
```
pip install mkdocs-awesome-pages-plugin
```
For using mermaid diagrams in mkdocs use the mermaid 2 plugin.  
```
pip install mkdocs-mermaid2-plugin
```

## MKDocs Mermaid Plugin and Fence config
There seem to be different configurations recommeded by the official doc pages, and then what others report as working config.  
```
markdown_extensions:
  - pymdownx.superfences:
      custom_fences:
        - name: mermaid
          class: mermaid
          format: !!python/name:mermaid2.fence_mermaid
```
versus  
```
markdown_extensions:
  - pymdownx.superfences:
      custom_fences:
        - name: mermaid
          class: mermaid
          format: !!python/name:mermaid2.fence_mermaid_custom
```