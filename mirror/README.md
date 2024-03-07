<div align="center">
<img height="150px" src="https://raw.githubusercontent.com/wisdom-oss/brand/main/svg/standalone_color.svg">
<h1>Mirroring Action</h1>
<h3>mirroring-action</h3>
<p>🪞 an action allowing the seamless mirroring of the organization into another repository</p>
</div>

This repository contains a composite GitHub Action allowing to automatically
push every incoming commit  into another repository on a GitLab Server.

## Usage
To use this action in your repository you need to use the following snippet:
```yaml
name: Mirror Repository
on: [push]
jobs:
  mirror:
    runs-on: ubuntu-latest
    steps:
      - uses: wisdom-oss/actions/mirror@main
        with:
          user: ${{ secrets.MIRROR_USER }}
          pat: ${{ secrets.MIRROR_PASSWORD }}
          repository: ${{ github.event.repository.name }}
          host: ${{ secrets.MIRROR_HOST }}
```