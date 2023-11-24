# Debian
```
wget -qO - https://releases.jfrog.io/artifactory/jfrog-gpg-public/jfrog\_public\_gpg.key | sudo apt-key add -
echo "deb https://releases.jfrog.io/artifactory/jfrog-debs xenial contrib" | sudo tee -a /etc/apt/sources.list;
apt update;
apt install -y jfrog-cli-v2-jf;
```

# Verify Install
```
$ jf --version
jf version 2.51.1
```

# jf cli 
```
$ jf
NAME:
   jf - See https://github.com/jfrog/jfrog-cli for usage instructions.

USAGE:
   jf [global options] command [command options] [arguments...]

VERSION:
   2.51.1

COMMANDS:
     access-token-create, atc  Creates an access token.
                                 By default, an user-scoped token will be created.
                                 Administrator may provide the scope explicitly with '--scope', or implicitly with '--groups', '--grant-admin'.
     help, h                   Shows a list of commands or help for one command

   Audit & Scan:
     audit, aud          Audit your local project's dependencies by generating a dependency tree and scanning it with Xray.
     build-scan, bs      Scan a published build-info with Xray.
     curation-audit, ca  Audit your project dependencies for their curation status.
     scan, s             Scan files located on the local file-system with Xray.

   Build Tools:
     docker                  Run any docker command, including ‘jf docker scan’ for scanning a local image with Xray.
     dotnet                  Run .NET Core CLI.
     dotnet-config, dotnetc  Generate dotnet configuration.
     go, go                  Runs go.
     go-config, goc          Generate go build configuration.
     go-publish, gp          Publish go package and/or its dependencies to Artifactory.
     gradle                  Run Gradle build.
     gradle-config, gradlec  Generate gradle build configuration.
     mvn                     Run Maven build.
     mvn-config, mvnc        Generate maven build configuration.
     npm                     Run npm command.
     npm-config, npmc        Generate npm configuration.
     nuget                   Run NuGet.
     nuget-config, nugetc    Generate nuget configuration.
     pip                     Run pip install.
     pip-config, pipc        Generate pip build configuration.
     pipenv                  Run pipenv install.
     pipenv-config, pipec    Generate pipenv build configuration.
     poetry                  Run poetry command
     poetry-config, poc      Generate poetry build configuration.
     terraform, tf           Runs terraform
     terraform-config, tfc   Generate terraform configuration.
     yarn                    Run Yarn commands.
     yarn-config, yarnc      Generate Yarn configuration.

   Lifecycle:
     release-bundle-create, rbc      Create a release bundle from builds or from existing release bundles
     release-bundle-distribute, rbd  Distribute a release bundle.
     release-bundle-promote, rbp     Promote a release bundle

   Other:
     rt          Artifactory commands.
     mc          Mission Control commands.
     xr          Xray commands.
     ds          Distribution commands.
     pl          JFrog Pipelines commands.
     completion  Generate autocomplete scripts.
     plugin      Plugins handling commands.
     config, c   Config commands.
     project     Project commands.
     ci-setup    Set up a CI pipeline with the JFrog Platform.
     options     Show all supported environment variables.
     login       Log in to a JFrog Platform via your web browser. Available for Artifactory 7.64.0 and above

GLOBAL OPTIONS:
   --help, -h     show help
   --version, -v  print the version
```

# Delete package from JFrog Artifactory using jf cli:
```
$ jf rt del nuget/Sustainsys.Saml2
```


# Search for package:
```
$ jf rt search nuget/Sus*
```
