## Flask Tutorial

Tutorial taken from [here](https://realpython.com/flask-by-example-part-1-project-setup/)

## Heroku 

Now we can push both of our apps live to Heroku.

- For staging: git push stage master
- For production: git push pro master

` heroku open --app <app-name>`

App names:
- app-test-pr
- app-stage-m

### Heroku Settings

Staging:
`heroku config:set APP_SETTINGS=config.ProductionConfig --remote stage`

Pro:
`heroku config:set APP_SETTINGS=config.ProductionConfig --remote pro`

## SSH

Original access denied, needed to generate new key and add to `.ssh` folder.

See [article](https://devcenter.heroku.com/articles/keys)

## Multiple Environments

This staging/production workflow allows us to make changes, show things to clients, experiment, etc. - all within a sandboxed server without causing any changes to the live production site that users are, well, using.

