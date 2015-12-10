It uses [hexo](https://hexo.io/). 

Ensure everything will be regenerated next time:
````
hexo clean
````

Generate::
````
hexo generate
````

The web is now located inside `public` folder.

Deploy without github ssh key configured:
````
hexo deploy
cd .deploy_git
git push -u https://github.com/StPhilipNeri/school-web.git HEAD:gh-pages --force
````
