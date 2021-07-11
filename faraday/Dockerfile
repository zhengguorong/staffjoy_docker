FROM bellsoft/liberica-openjdk-alpine-musl:11

COPY ./target/faraday-1.0.0.jar /usr/app/

WORKDIR /usr/app

RUN sh -c 'touch faraday-1.0.0.jar'

ENTRYPOINT ["java", "-jar", "faraday-1.0.0.jar"]