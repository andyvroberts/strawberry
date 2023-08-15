# strawberry
A static web-site using github pages

## Hugo 
Install hugo by downloading the latest debian package.  
https://github.com/gohugoio/hugo/releases/

```
sudo apt install ./hugo_extended_0.117.0_linux-amd64.deb
```
Note: You will need the extended version of Hugo to run some of the CSS pre-processors and other tools.  

Add the installation location to your path in the .profile   
```
which hugo
>$ /usr/local/bin/hugo
```

Now create your new Hugo project.  As you are adding this to your github project, use the --force flag as the readme.md file will already exist (Hugo expects an empty or new folder).  
```
hugo new site ./ --force
```
