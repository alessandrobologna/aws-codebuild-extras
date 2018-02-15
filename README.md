# aws-codebuild-extras ![Build Status](https://codebuild.us-east-1.amazonaws.com/badges?uuid=eyJlbmNyeXB0ZWREYXRhIjoiS2NyUEZXUjJUQ2ZqRi9HeVFIWE5FWldMK1VOb29xbmVZWjBpdG9VV0ZDc2ZiRVdMcXJ1b3lML0hEWk9XS0hlL2xjM0V5NHVwZEdoSWZDMHRpV1NsQkxvPSIsIml2UGFyYW1ldGVyU3BlYyI6InRVa01aeDVFM05ja3hOT0EiLCJtYXRlcmlhbFNldFNlcmlhbCI6MX0%3D&branch=master)
Add extra information of your AWS CodeBuild build via environment variables.

## Usage

Add the following commands to the `install` or `pre_build` phase of your buildspec, as below:
```yaml
version: 0.2

phases:
  install:
    commands:
      - curl -fsSL -o /tmp/install https://raw.githubusercontent.com/alessandrobologna/aws-codebuild-extras/master/install
      - . /tmp/install
  build:
    commands:
      - env
```
