# Setup
A static web-site using github pages

## Installations
### Python
If you need to add Python, as I do on Alpine, run:
```python
doas apk add python3 py3-pip
mkdir new mkdocs
cd mkdocs
py -m venv .venv/docs
source .venv/docs/bin/activate
# optional
py -m pip install -r ../req.txt 
```
### MkDocs
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

