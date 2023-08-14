# strawberry
A static web-site using github pages

## Hugo 
Install hugo by downloading the latest debian package.  
https://github.com/gohugoio/hugo/releases/

```
sudo apt install ./hugo_0.117.0_linux-amd64.deb
```

Add the installation location to your path in the .profile   
```
which hugo
>$ /usr/local/bin/hugo
```

Now create your new Hugo project.  As you are adding this to your github project, use the --force flag as the readme.md file will already exist (Hugo expects an empty or new folder).  
```
hugo new site ./ --force
```
