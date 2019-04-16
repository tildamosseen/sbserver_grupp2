# Systembolagsserver

Systembolagsservern innehåller en maveniserad version av systembolagsservern ni arbetat med i TIG058.

Maven strukturerar källkoden på ett specifikt sätt, det är viktigt att hålla sig till strukturen för att programmet ska fungera.

Strukturen är som följer, detaljerad förklaring nedan
```
├── pom.xml
├── readme.md
└── src
    ├── main
    │   ├── java
    │   │   └── se
    │   │       └── gu
    │   │           └── ait
    │   │               └── sbserver
    │   │                   ├── domain
    │   │                   │   └── Product.java
    │   │                   ├── main
    │   │                   │   ├── TestJsonExporter.java
    │   │                   │   ├── TestProductLine.java
    │   │                   │   ├── TestSQLInsertExporter.java
    │   │                   │   ├── TestStreams.java
    │   │                   │   └── TestSwing.java
    │   │                   ├── servlet
    │   │                   │   ├── Constraint.java
    │   │                   │   ├── Formatter.java
    │   │                   │   ├── FormatterFactory.java
    │   │                   │   ├── JsonFormatter.java
    │   │                   │   ├── ParameterParser.java
    │   │                   │   ├── SystemetAPIv1.java
    │   │                   │   └── SystemetWebAPI.java
    │   │                   └── storage
    │   │                       ├── AbstractProductExporter.java
    │   │                       ├── CSVHelper.java
    │   │                       ├── DBHelper.java
    │   │                       ├── FakeProductLine.java
    │   │                       ├── JsonExporter.java
    │   │                       ├── ProductGroupExporter.java
    │   │                       ├── ProductGroups.java
    │   │                       ├── ProductLine.java
    │   │                       ├── ProductLineFactory.java
    │   │                       ├── SQLBasedProductLine.java
    │   │                       ├── SQLInsertExporter.java
    │   │                       ├── XMLBasedProductLine.java
    │   │                       └── package-info.java
    │   ├── resources
    │   │   ├── bolaget.db
    │   │   ├── log4j2.xml
    │   │   └── products.csv
    │   └── webapp
    │       └── WEB-INF
    │           ├── WEB-INF.iml
    │           ├── api.html
    │           ├── search.html
    │           ├── style.css
    │           └── web.xml
    └── test
        └── java
```

1. `````pom.xml````` pomfilen är Mavens konfigurationsfil för projektet. Filen innehåller information som Maven behöver för att kompilera projektet. Om man behöver använda externa bibliotek behöver dessa skrivas in i pomfilen. Med allra största sannolikhet kommer ni inte att behöva ändra något i filen, information om hur filen är uppbyggd finns [här](https://maven.apache.org/guides/introduction/introduction-to-dependency-mechanism.html) 
1. `````readme.md````` filen som innehåller texten som ni läser nu. Detta är ingen mavenfil utan en fil som beskrivet innehållet i ett github-repository.
1. `````src/````` mappen src är mappen under vilken all källkod ligger.
1. `````readme.md`````
1. `````readme.md`````
## Kompileringsinstruktioner

För att kompilera systembolagsservern behöver ni har Maven installerat på era datorer. Instruktioner för att installera Maven finns nedan.




## Installera Maven

###  Maven i macOS
För att installera Maven i macOS kör ni kommandot
```brew install maven```

### Maven i Windows / CygWin
Följ instruktionerna på denna sida för att installera Maven i Windows:
[https://geekforum.wordpress.com/2015/03/19/install-git-and-maven-for-cygwin/](https://geekforum.wordpress.com/2015/03/19/install-git-and-maven-for-cygwin/) 

### Maven i Linux
Använd den pakethanterare som din linuxdist använder, exempelvis ````apt-get````