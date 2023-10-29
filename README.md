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

### gerando jar com módulo javafx

Embora não atendam ao propósito, as realizações executadas por [este tutorial](https://www.youtube.com/watch?v=dLH-HjiCtaI) criaram um executável (exe) funcional para o JavaFX no caminho `build\jpackage\helloworld`, apesar de dar erro ao executar o comando de build `gradle jpackage`

##### Outro plugin

O Plugin `id 'com.github.johnrengelman.shadow' version '8.1.1'` não requer nenhuma alteração, executando juntamente com o `id 'org.openjfx.javafxplugin' version '0.1.0'` e gera, na pasta build/lib, um arquivo `jar` no formato `FatJar` que inclui todas as dependências necessárias para a execução do jar. (localizar arquivo de final `-all.jar`)