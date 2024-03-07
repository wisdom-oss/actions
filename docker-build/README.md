<div align="center">
<img height="150px" src="https://raw.githubusercontent.com/wisdom-oss/brand/main/svg/standalone_color.svg">
<h1>Build Docker Image</h1>
<h3>actions/</h3>
<p>🧪 an action for building docker images with consistent tagging</p>
</div>

This action builds a Docker Image which is then pushed to a configurable
container registry.
The default registry is `ghcr.io`.

## Usage
To use this action in your repository you need to use the following snippet:
```yaml
name: Build Docker Image
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: wisdom-oss/actions/docker-build@main        
```