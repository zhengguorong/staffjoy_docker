FROM bellsoft/liberica-openjdk-alpine-musl:11

COPY ./target/sms-svc-1.0.0.jar /usr/app/

WORKDIR /usr/app

RUN sh -c 'touch sms-svc-1.0.0.jar'

ENTRYPOINT ["java", "-jar", "sms-svc-1.0.0.jar"]