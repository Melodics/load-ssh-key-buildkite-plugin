# Load SSH Key Buildkite Plugin

Loads a SSH key from AWS secret as an environment hook.

## Example

Add the following to your `pipeline.yml`

```yml
steps:
    - command: 'my command',
      plugins:
        melodics/load-ssh-key
```

## Requirements

For this to run, you will need to:

- Set the `AWS_DEFAULT_REGION` environment variable
- Set the `SSH_KEY_SECRET_NAME` environment variable
  - This must be the name of a secret containing a base64 encoded private
    ssh key stored in the secret binary
- Have the AWS cli installed on your agent and authenticated to access the
  secret with the given name