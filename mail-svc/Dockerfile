FROM bellsoft/liberica-openjdk-alpine-musl:11

COPY ./target/mail-svc-1.0.0.jar /usr/app/

WORKDIR /usr/app

RUN sh -c 'touch mail-svc-1.0.0.jar'

ENTRYPOINT ["java", "-jar", "mail-svc-1.0.0.jar"]