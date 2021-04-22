Drone plugin to upload coverage reports to Codacy. You are able to upload the
supported coverage report formats automatically to Codacy as part of your
pipelines.

## Examples

```yaml
kind: pipeline
name: default

steps:
- name: step name
  image: dronehippie/codacy:1
  settings: []
```

## Parameters

dummy
: dummy
