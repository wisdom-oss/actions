<div align="center">
<img height="150px" src="https://raw.githubusercontent.com/wisdom-oss/brand/main/svg/standalone_color.svg">
<h1>Go Test Report</h1>
<h3>action/go-tests</h3>
<p>🧪 an action for posting test results on a </p>
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
    permissions:
      checks: write
      pull-requests: write
      issues: read
      contents: read
    steps:
      - uses: wisdom-oss/actions/go-test@main
        env:
          # Put the environment variables you need here
```