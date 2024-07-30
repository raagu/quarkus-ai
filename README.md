# quarkus-ai

This project uses Quarkus, the Supersonic Subatomic Java Framework.

If you want to learn more about Quarkus, please visit its website: <https://quarkus.io/>.

## Running the application in dev mode

You can run your application in dev mode that enables live coding using:

```shell script
./gradlew quarkusDev
```

> **_NOTE:_**  Quarkus now ships with a Dev UI, which is available in dev mode only at <http://localhost:8080/q/dev/>.

## Packaging and running the application

The application can be packaged using:

```shell script
./gradlew build
```

It produces the `quarkus-run.jar` file in the `build/quarkus-app/` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `build/quarkus-app/lib/` directory.

The application is now runnable using `java -jar build/quarkus-app/quarkus-run.jar`.

If you want to build an _über-jar_, execute the following command:

```shell script
./gradlew build -Dquarkus.package.jar.type=uber-jar
```

The application, packaged as an _über-jar_, is now runnable using `java -jar build/*-runner.jar`.

## Creating a native executable

You can create a native executable using:

```shell script
./gradlew build -Dquarkus.native.enabled=true
```

Or, if you don't have GraalVM installed, you can run the native executable build in a container using:

```shell script
./gradlew build -Dquarkus.native.enabled=true -Dquarkus.native.container-build=true
```

You can then execute your native executable with: `./build/quarkus-ai-1.0.0-runner`

If you want to learn more about building native executables, please consult <https://quarkus.io/guides/gradle-tooling>.

## Related Guides

- REST ([guide](https://quarkus.io/guides/rest)): A Jakarta REST implementation utilizing build time processing and Vert.x. This extension is not compatible with the quarkus-resteasy extension, or any of the extensions that depend on it.
- LangChain4j Hugging Face ([guide](https://docs.quarkiverse.io/quarkus-langchain4j/dev/index.html)): Provides integration of Quarkus LangChain4j with the Hugging Face API
- LangChain4j Redis embedding store ([guide](https://docs.quarkiverse.io/quarkus-langchain4j/dev/index.html)): Provides the Redis Embedding store for LangChain4j
- REST Jackson ([guide](https://quarkus.io/guides/rest#json-serialisation)): Jackson serialization support for Quarkus REST. This extension is not compatible with the quarkus-resteasy extension, or any of the extensions that depend on it
- Quarkus LangChain4j pgvector embedding store ([guide](https://docs.quarkiverse.io/quarkus-langchain4j/dev/index.html)): Provides the pgvector Embedding store for Quarkus LangChain4j
- LangChain4j Easy RAG ([guide](https://docs.quarkiverse.io/quarkus-langchain4j/dev/index.html)): Provides the Easy RAG functionality with LangChain4j
- LangChain4j Ollama ([guide](https://docs.quarkiverse.io/quarkus-langchain4j/dev/index.html)): Provides the basic integration of Ollama with LangChain4j
- LangChain4j ([guide](https://docs.quarkiverse.io/quarkus-langchain4j/dev/index.html)): Provides the basic integration with LangChain4j

## Provided Code

### REST

Easily start your REST Web Services

[Related guide section...](https://quarkus.io/guides/getting-started-reactive#reactive-jax-rs-resources)