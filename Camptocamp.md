Setup for Camptocamp project sites
==================================


```shell
$ hugo new site hugo
$ git submodule add git@github.com:camptocamp/hugo-elate-theme.git hugo/themes/elate
$ echo 'theme = "elate"' >> hugo/config.toml 
$ touch hugo/content/.placeholder
$ git add hugo
$ echo "hugo/public" >> .gitignore
$ git commit -m "Add hugo"
 
$ git checkout --orphan gh-pages
$ git reset --hard
$ git commit --allow-empty -m "Initializing gh-pages branch"
$ git push -u origin gh-pages 
 
$ git checkout master 
$ git worktree add -B gh-pages hugo/public gh-pages
```
