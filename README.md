## Flask Tutorial

Deployment [tutorial](https://opensource.com/article/18/1/running-python-application-kubernetes)

Tutorial taken from [here](https://realpython.com/flask-by-example-part-1-project-setup/)

Other tutorial [here](https://github.com/honestbee/flask_app_k8s)

[Beginner](https://github.com/docker/labs/tree/bd6bcaa1e25e75dc3611ea063b3d38c65e205141/beginner/flask-app) Flask App

[Google](https://cloud.google.com/kubernetes-engine/docs/tutorials/hello-app)

## Heroku 

Now we can push both of our apps live to Heroku.

- For staging: `git push stage master`

- For production: `git push pro master`

` heroku open --app <app-name>`

App names:
- app-test-pr
- app-stage-m

### Heroku Settings

Staging:
`heroku config:set APP_SETTINGS=config.ProductionConfig --remote stage`

Pro:
`heroku config:set APP_SETTINGS=config.ProductionConfig --remote pro`

Config seetings:

Staging:
`heroku run python app.py --app app-stage-m`

Pro:
`heroku run python app.py --app app-test-pr`

## SSH

Original access denied, needed to generate new key and add to `.ssh` folder.

See [article](https://devcenter.heroku.com/articles/keys)

## Multiple Environments

This staging/production workflow allows us to make changes, show things to clients, experiment, etc. - all within a sandboxed server without causing any changes to the live production site that users are, well, using.

## Local settings

Didn't work originally.  So did the install per [repo page](https://github.com/kennethreitz/autoenv), updated `.bashrc` file and setup the `.env` file.

```bash
brew install autoenv
echo "source $(brew --prefix autoenv)/activate.sh" >> ~/.bash_profile
```

The command missing to make it work, within the project directory:
`virtualenv ENV`

## Google Cloud

Deploying instructions taken from [here](https://cloud.google.com/community/tutorials/envoy-flask-google-container-engine)

### 1. Get Google Cloud Account [here](https://console.cloud.google.com/projectselector/kubernetes/list?supportedpurview=project)
### 2. Need `Kubect1` so:
	- `brew install kubernetes-cli`
	- `brew install docker`




