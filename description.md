## Gradle Configuration
Gradle is a tool for automating building.  
The Gradle build file `build.gradle.kts` located in the main directory specifies Gradle's configuration for this project.

The build file consists of 4 main sections:
- Plugins
- Repositories
- Dependencies
- Kotlin
	- Kotlin compiler options

### Plugins
Plugins are extensions that add features to Gradle.
In this project we add plugins for [Kotlin](https://github.com/JetBrains/kotlin) and [SpringBoot](https://github.com/spring-projects/spring-boot).

### Repositories
In this section the repository for solving dependencies is declared.  
In our case, `mavenCentral()` specifies that the [Maven Central public repository](https://repo.maven.apache.org/maven2/) will be used to solve dependencies.

### Dependencies
This sections contains the dependencies of the project which will be downloaded from the repository specified in the previous section.  
The dependencies used in this project are:
- [SpringBoot](https://github.com/spring-projects/spring-boot)
- [Jackson](https://github.com/FasterXML/jackson)
- [Kotlin Reflection](https://kotlinlang.org/docs/reflection.html#jvm-dependency)
- Kotlin Standard Library JDK 8 extension
- [Bootstrap WebJar](https://github.com/webjars/bootstrap)

### Kotlin
Kotlin is configured to run on the JVM.
When the Kotlin targets the JVM platform, options of the compile task are specified in the `compileKotlin` variable.
In our case, we specify that the target version of the JVM is 11 with `jvmTarget` and we configure the compiler to generate error by adding the `-Xjsr305=strict` flag.

