# This is repository for framed github action

## Github Action

You can use framed as a github action to verify your project structure. Minimal example:

```yaml
name: Verify Project Structure
on: [push, pull_request]
jobs:
verify:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - name: Verify Project Structure
        uses: mactat/framed@0.0.8
        with:
        template: './framed.yaml' # Optional, default is framed.yaml
        version: 'v0.0.7'         # Optional, default is v0.0.7
```
