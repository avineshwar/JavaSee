# JQuerly

Query Method Calls from Java Programs.  It's Java version of querly https://github.com/soutaro/querly

## Installation

JQuerly requires Java(JDK) 11 or later and Gradle 5.0 or later.

1. Install JDK 11 or later
2. Install Gradle 5.0 or later
3. Type `$ gradle shadowjar`
4. You can found jquerly-all.jar on `build/libs/`

## Quick start

As a first step, you can write the following YAML file

```yaml
rules:
  - id: jquerly.example
    pattern:
      - _.println(_)
    message: |
      Trap println() method.
```

and save it to `jquerly.yaml`

Next you can run `jquerly check` command to **jquerly** patterns against your code base.

```
$ java -jar build/libs/jquerly-all.jar check -config jquerly.yaml
```
