# container-python-dev
Creating a docker image for dbt development

### Using dbt-env

1. To install run
    ```shell
    docker pull ghcr.io/aaron-ortega/dbt-env:latest
    ```

2. Configure your startup environment (eg. bash_profile, .zshrc, etc.) to include
    ```shell
    alias dbt-docker="docker container run --env-file=$HOME/.env -p 8080:8080 -it --entrypoint=/bin/bash -v \"$PWD\":/home dbt-env"
    ```

3. Run `dbt-docker` in the directory where the dbt project is located