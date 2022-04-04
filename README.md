# Technical test for Devops position at Connecting Food
## Tasks
* Create a Dockerfile to package the application  (**source code in app directory of current repository**)
  * The application runs with **python 3.5**
  * The application runs with an embedded database, but the schema must be created (either at build or runtime) with:
    ```bash
    python manage.py migrate
    ```
  * To start the application:
    ```bash
    python manage.py runserver
    ```
* Prepare a simple helm chart, with deployment and service objects to run this application
* Create a Github Actions worfklow that will build and push a Docker image running the Django app
  * Image should be pushed on your personal repository on docker hub (https://hub.docker.com/) 
## Submission
Helm chart and workflow should be saved on a private `candidate/connecting-food-devops-test` repository on your github account.
Access should be granted to 2 members of the `connecting-food` group:
* <https://github.com/nmilon-cf>
* <https://github.com/jhammout02>
## Expected repo structure
```bash
$ tree .
.
├── .github
│   └── workflows
│       └── workflow.yml
├── app
│   └── Dockerfile
│   └── requirements.txt
│   └── ...
└── helm
    └── Chart.yaml
    └── values.yaml
    └── templates
```