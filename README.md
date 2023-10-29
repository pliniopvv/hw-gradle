## Hello Gradle

````groovy
task hellogradle() {
    println("Hello Gradle ...")
}
````

fonte: https://www.youtube.com/watch?v=WPqN306rBZE&list=PL7R_QxClgM0SOesf9kRNnA1AEuKFsdQuX

## Plugin 'java'

```groovy
apply plugin: 'java'

or

plugins {
    id 'java'
}
```

fonte: https://www.youtube.com/watch?v=GbQIeFpf8z8&list=PL7R_QxClgM0SOesf9kRNnA1AEuKFsdQuX&index=3

## main class in jar

```groovy
jar {
    manifest {
        attributes(
            'Main-Class': 'Main'
        )
    }
}
```

fonte: https://www.youtube.com/watch?v=GbQIeFpf8z8&list=PL7R_QxClgM0SOesf9kRNnA1AEuKFsdQuX&index=3

## dependencies 

```groovy
repositories {
    mavenCentral()
}

dependencies {
    // TODO MAVEM DEPENDENCIES   
}
```

## plugin application

```groovy
plugins {
    id 'application'
}
```

## application javafx

[Tutorial do youtube](https://www.youtube.com/watch?v=bRpGnCjJ0ro)
[Plugin github](https://github.com/openjfx/javafx-gradle-plugin)

É necessária a adição da linha abaixo, invés da `jar{ ... } `

Recomendavel verificar configurações adicionais disponíveis no github do plugin Gradle.

- Necessário executar o `build` para `run`

```groovy 
mainClassName = "Main"
```