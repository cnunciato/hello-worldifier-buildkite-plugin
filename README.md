Buildkite Hello Worldifier

This is the minimum content of the README (minus this paragraph and the command that follows) required to pass the linter. To run the linter for this particular plugin, I had to run:

```bash
docker run -it --rm -v "$PWD:/plugin:ro" --platform linux/amd64 buildkite/plugin-linter --id cnunciato/hello-worldifier
```

```yml
steps:
  - command: echo "Hey, girl."
    plugins:
      - cnunciato/hello-worldifier#v0.0.1:
          greeting: Hello, world!
```