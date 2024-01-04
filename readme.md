# Maven Site Deployment Action

Builds and deploys a Maven site.

## Inputs

| Input    | Description                               | Required                             |
|----------|-------------------------------------------|--------------------------------------|
| host     | Host where the site will be deployed.     | True                                 |
| url      | URL to deploy the site.                   | True                                 |
| username | Username for the deployment server.       | True                                 |
| password | Password for the deployment server.       | True                                 |
| jdk      | JDK version to use.                       | False, defaults to '11'              |
| profile  | Maven profile for site deployment.        | False, defaults to 'deployment-site' |

## Usage

This builds and deploys the Maven site.

```
jobs:
  deploy:
    name: Deployment
    runs-on: ubuntu-latest

    steps:
    - name: Deploy site
      uses: bernardo-mg/maven-site-deployment-action@v1
      with:
        host: ${{ inputs.host }}
        url: ${{ secrets.url }}
        username: ${{ secrets.username }}
        password: ${{ secrets.password }}
```

## Collaborate

Any kind of help with the project will be well received, and there are two main ways to give such help:

- Reporting errors and asking for extensions through the issues management
- or forking the repository and extending the project

### Issues management

Issues are managed at the GitHub [project issues tracker][issues], where any Github user may report bugs or ask for new features.

### Getting the code

If you wish to fork or modify the code, visit the [GitHub project page][scm], where the latest versions are always kept. Check the 'master' branch for the latest release, and the 'develop' for the current, and stable, development version.

## License
The project has been released under the [MIT License][license].

[issues]: https://github.com/Bernardo-MG/maven-site-deployment-action/issues
[license]: https://www.opensource.org/licenses/mit-license.php
[scm]: https://github.com/Bernardo-MG/maven-site-deployment-action
