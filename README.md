# This is repository for framed github action

## Framed

Framed is a CLI tool that simplifies the organization and management of files and directories in a reusable and architectural manner. It provides YAML templates for defining project structures and enables workflows based on those.

To always be in sync with the YAML template, Framed provides a built-in test command that can be used in CI/CD pipelines to verify the project structure.

You can find more information about Framed [here](https://github.com/mactat/framed)

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
        uses: mactat/framed@0.0.7
        with:
        template: './framed.yaml' # Optional, default is framed.yaml
        version: 'v0.0.7'         # Optional, default is v0.0.7
```
