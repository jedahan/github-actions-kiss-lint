### With a top-level repository


```yaml
#.github/workflow/lint.yaml
on: [pull_request, workflow_dispatch]

jobs:
  lint:
    runs-on: ubuntu-20.04

    steps:
      - uses: actions/checkout@v2
      - uses: actions/kiss-lint
```

### For multiple subdirectories

```yaml
#.github/workflow/lint.yaml
on: [pull_request, workflow_dispatch]

jobs:
  lint:
    runs-on: ubuntu-20.04

    steps:
      - uses: actions/checkout@v2
      - uses: actions/kiss-lint
        with:
          kiss-path: core:extra:wayland
```
