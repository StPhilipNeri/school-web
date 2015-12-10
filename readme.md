It uses [hexo](https://hexo.io/).

Important: I had to patch node_modules/hexo/lib/plugins/helper/url_for.js file becuase it returned wrong path when called with no parameter. The latest unreleased url_for.js was [this one](https://github.com/hexojs/hexo/blob/534102e6992bfb4df975a724846993617edcf988/lib/plugins/helper/url_for.js) at the time. This affected link on top picture.

This should not be needed once hexo releses next version.

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
