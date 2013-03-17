
# Go for it: Build your artefacts!
Clean build, also invoking unit tests:
> mvn clean install

Clean build, without unit tests:
> mvn clean install -DskipTests=true


# Deploy to rascal-mpl update site
1. > cd rascal-update-site
2. > mvn install -P upload2rascalmpl
