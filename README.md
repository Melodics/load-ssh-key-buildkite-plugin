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

- Set the `SSH_KEY_SECRET_NAME` environment variable
- Have the AWS cli installed on your agent and authenticated to access the
  secret with the given name