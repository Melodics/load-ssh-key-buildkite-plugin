# Load SSH Key Buildkite Plugin

Loads a SSH key from AWS secret as an environment hook.

## Example

Add the following to your `pipeline.yml`

```yml
steps:
    - command: 'my command',
      plugins:
        melodics/load-ssh-key:
          secret: "my-secret-name"
```

## Requirements

For this to run, you will need to:

- Set the `AWS_DEFAULT_REGION` environment variable
- Provide the name of the secret via the `secret` configuration property
- Have the AWS cli installed on your agent and authenticated to access the
  secret with the given name
