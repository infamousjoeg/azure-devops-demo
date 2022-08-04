# azure-devops-demo
A demonstration using @cyberark Conjur's Azure DevOps Pipelines integration

## Setup

The Conjur Service Connection service connection needs to be configured prior to executing the pipeline.

![image](https://user-images.githubusercontent.com/1924063/182889057-252edc86-cfbc-49b8-9f21-182eade6c2c5.png)

## How it works

The Conjur Service Connection contains all the connection and secret information needed to securely retrieve a secret just-in-time from Conjur.  The secret value is then presented to the running pipeline as an environment variable defined within the service connection.  You may reference that variable from within the pipeline script to utilize the secret.

## License

[MIT](LICENSE)
