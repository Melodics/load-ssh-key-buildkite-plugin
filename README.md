# Load SSH Key Buildkite Plugin

Loads a SSH key from AWS secret as an environment hook.

## Example

Add the following to your `pipeline.yml`

```yml
steps:
  - command: ls
    plugins:
      - melodics/load-ssh-key#v0.0.4:
          secret: "my-secret-name"
```

## Requirements

For this to run, you will need to:

- Set the `AWS_DEFAULT_REGION` environment variable
- Have the AWS CLI installed in your buildkite agent

## Configuration

### `secret` (Required, string)

The name of the secret containing your SSH key. The AWS CLI used by your agent
must be pre-authenticated to access this secret.
