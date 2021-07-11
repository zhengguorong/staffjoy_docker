FROM bellsoft/liberica-openjdk-alpine-musl:11

COPY ./target/whoami-svc-1.0.0.jar /usr/app/

WORKDIR /usr/app

RUN sh -c 'touch whoami-svc-1.0.0.jar'

ENTRYPOINT ["java", "-jar", "whoami-svc-1.0.0.jar"]