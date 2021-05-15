FROM  adoptopenjdk/openjdk11:alpine
WORKDIR /app/backend
ENV JAR_TARGET "app.jar"
# 起動コマンドをシェル環境で実行
ENTRYPOINT ["sh","-c","java -jar -Dspring.profiles.active=docker-compose ./target/${JAR_TARGET}"]
# COPY ./target/app.jar ./app.jar
# CMD ["/usr/bin/java", "-jar", "app.jar"]