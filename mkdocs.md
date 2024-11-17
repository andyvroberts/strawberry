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

## 