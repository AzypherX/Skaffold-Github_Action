
## Overall structure and flow of the Repo


### Flow
- sample flask web app
- build the docker image
- push it to github
- which triggers github actions to build the code and push the image to google artificate registry
- use skaffold to deploy the app to kubernetes
- skaffold inside use the manifest.yml file to collects the metadata and all
- At last create a deployement and service in the GKE cluster




### structure

- .github/workflows
    - google.yml -> uses the below order file [skaffold.yml]
        - skaffold.yml -> uses the [manifest.yml] file
            - manifest.yml