THIS BRANCH IS FOR TESTING

To build:

1. Copy the [`docs/include` dir](https://github.com/elastic/logstash/tree/main/docs/include) from elastic/logstash to this repo under `docs/plugins/`. The final dirpath should be `docs/plugins/include`.

1. Copy the [`docs/static/core-plugins dir`](https://github.com/elastic/logstash/tree/main/docs/static/core-plugins) from elastic/logstash to this repo under `docs/plugins`. The final dirpath should be `docs/plugins/static/core-plugins/`.

2. Find and replace:
  Find: `../../../../logstash/docs/include`
  Replace: `../include`

1. Find and replace:
  Find: `../../../logstash/docs/static/`
  Replace:`./static/`

1. Find and replace:
  Find: `../../include`
  Replace: `../../../include`

```
$GIT_HOME/docs/build_docs --doc $GIT_HOME/logstash-docs/docs/plugins/index.asciidoc --chunk 1
```