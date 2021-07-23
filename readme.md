### For top-level repository


```yaml
#.github/workflow/lint.yaml
name: lint packages

on:
  pull_request:
  workflow_dispatch:

jobs:
  lint_packages:
    runs-on: ubuntu-20.04

    steps:
      - name: lint some packages
        uses: actions/kiss-lint
```

### For multiple subdirectories

```yaml
#.github/workflow/lint.yaml
name: lint packages

on:
  pull_request:
  workflow_dispatch:

jobs:
  lint_packages:
    runs-on: ubuntu-20.04

    steps:
      - name: lint some packages
        uses: actions/kiss-lint
        kiss_path: core:extra:wayland
```
