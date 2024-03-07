<div align="center">
<img height="150px" src="https://raw.githubusercontent.com/wisdom-oss/brand/main/svg/standalone_color.svg">
<h1>Go Test Report</h1>
<h3>action/go-tests</h3>
<p>🧪 an action for generating Documentation files from Go in-code documentation</p>
</div>

This action generates documentation files using `github.com/princjef/gomarkdoc`
and uploads them as artifact named `documentation` to the pipeline

## Usage
To use this action in your repository you need to use the following snippet:
```yaml
name: Mirror Repository
on: [push]
jobs:
  mirror:
    runs-on: ubuntu-latest
    steps:
      - uses: wisdom-oss/actions/go-docs@main
```