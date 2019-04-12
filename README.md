## Python SDK for SecureDrop

[![CircleCI](https://circleci.com/gh/freedomofpress/securedrop-sdk/tree/master.svg?style=svg)](https://circleci.com/gh/freedomofpress/securedrop-sdk/tree/master)

This SDK provides a convenient Python interface to the [SecureDrop Journalist Interface API](https://docs.securedrop.org/en/latest/development/journalist_api.html). The development of the SDK was primarily motivated by the creation of the [SecureDrop Workstation](https://github.com/freedomofpress/securedrop-workstation) based on Qubes OS.

The SDK is currently used by the [SecureDrop Client](https://github.com/freedomofpress/securedrop-client) that is a component of the SecureDrop Workstation. When used in Qubes OS, the SDK uses the [securedrop-proxy](https://github.com/freedomofpress/securedrop-proxy) service, as the VM which runs the client does not have network access by design.

**IMPORTANT:** This project is still under active development. We do not recommend using it in any production context.

### Development

This project uses [pipenv](https://docs.pipenv.org) to manage all dependencies.
This is a Python 3 project. When using `pipenv` locally, ensure you used the `--keep-outdated` flag to prevent
dependencies from being unnecessarily upgraded during normal development.

We cover all the API calls supported by the SecureDrop Journalist Interface API.

Additional tests will be added in future.

### Testing

To test the code, you will need to run the SecureDrop `make dev` command on the same system. The test suite for
this project will test against that development container.

### Release

To make a release, you should:

1. Update the version in `setup.py`.
2. Update the changelog.
3. Commit the changes, and `git tag`.
4. Create a PR, push the new tag, and get the PR reviewed and merged into `master`.
5. Push the new release to the PSF's PyPI [following this documentation](https://packaging.python.org/tutorials/packaging-projects/#uploading-the-distribution-archives).

### License: GPLv3+
