FROM bellsoft/liberica-openjdk-alpine-musl:11

COPY ./target/ical-svc-1.0.0.jar /usr/app/

WORKDIR /usr/app

RUN sh -c 'touch ical-svc-1.0.0.jar'

ENTRYPOINT ["java", "-jar", "ical-svc-1.0.0.jar"]