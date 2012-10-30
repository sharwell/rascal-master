# Manually installing lpg.runtime.java [^why]
1. Download [lpg.runtime.java_2.0.18.jar](http://download.eclipse.org/technology/imp/updates/plugins/lpg.runtime.java_2.0.18.jar).
2. Install it to your local maven repository: 
> mvn install:install-file -DgroupId=lpg.runtime.java -DartifactId=lpg.runtime.java -Dversion=2.0.18 -Dpackaging=jar -Dfile=/path/to/lpg.runtime.java_2.0.18.jar

[^why]: The IMP repository is not yet a p2 repository. Thus, e.g. the required bundle *lpg.runtime.java;bundle-version="2.0.18”* cannot resolved via the tycho p2 target platform resolver.


# Go for it: Build your artefacts!
Clean build, also invoking unit tests:
> mvn clean install

Clean build, without unit tests:
> mvn clean install -DskipTests=true


# Deploy to rascal-mpl update site
1. > cd rascal-update-site
2. > mvn install -P upload2rascalmpl