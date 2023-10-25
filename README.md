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