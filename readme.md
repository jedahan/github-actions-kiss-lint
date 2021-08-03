### With a top-level repository


```yaml
#.github/workflow/lint.yaml
on: [pull_request, workflow_dispatch]

jobs:
  lint:
    runs-on: ubuntu-20.04

    steps:
      - uses: actions/checkout@v2
      - uses: actions/kiss-lint@v3
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
      - uses: actions/kiss-lint@v3
        with:
          kisspath: core:extra:wayland
```
