# cogitate-data
Documentation repo for Cogitate data Release
- Clone repo
- Install dependencies
```shell
pipenv install
```
- Run
```shell
pipenv run mkdocs serve
```
All source files live in **docs**  
All built files live in **site** [gitignored]

To deploy to gh-pages
```shell
pipenv run mkdocs gh-deploy
```  
This will build current repo (even if not committed), commit locally to the gh-pages branch, and push it to remote.  
NB: Make sure to remeber to commit to master first.