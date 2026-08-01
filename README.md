# Bruno API testing tool CLI demonstration

[![Testing passing](https://github.com/guipastl/bruno-cli-demo/actions/workflows/bruno-api-tests.yml/badge.svg)](https://github.com/guipastl/bruno-cli-demo/actions/workflows/bruno-api-tests.yml)

This repository demonstrates how to run Bruno API tests in CI/CD with GitHub Actions and the Bruno CLI against the public Gorest API.

## What this demo covers
- Bruno collections for CRUD-style API checks against https://gorest.co.in/
- GitHub Actions execution through the Bruno CLI
- HTML test reporting generated during the workflow run
- A simple setup for validating API health automatically on push, pull request, and manual runs

## CI/CD workflow
The workflow in [.github/workflows/bruno-api-tests.yml](.github/workflows/bruno-api-tests.yml) performs the following steps:
1. Checks out the repository
2. Creates a temporary environment file with the GitHub secret value for ACCESS_TOKEN
3. Runs the Bruno collection with the test environment
4. Publishes the generated HTML report as a workflow artifact

## Local execution
Run the collection locally from the demo folder:

```bash
cd collections/demo
bruno run --env test
```

___

Developed with 💚 by [Guilherme](https://www.linkedin.com/in/guipastl).