# azure-devops-demo
A demonstration using @cyberark Conjur's Azure DevOps Pipelines integration

## How it works

1. Pipeline is triggered within Azure DevOps Pipelines or via commit trigger.
2. The GitHub repository is downloaded into a working environment created on a self-hosted agent pool.
3. The `GetSecret` step authenticates to the Conjur service as the provided Host Identity.
4. The integration then looks within the root directory of the workspace for a [secrets.yml](secrets.yml) file.
5. If the [secrets.yml](secrets.yml) file is detected, it is read. This file defines the environment variable key and the secret variable path in Conjur to give as. (e.g. `ENV_VAR: !var path/to/secret/variable`)
6. The final step `echo`s `SECRET1` and `SECRET2` to STDOUT while `sed` adds a space between each char to prevent masking for demonstration purposes.

## License

[MIT](LICENSE)
