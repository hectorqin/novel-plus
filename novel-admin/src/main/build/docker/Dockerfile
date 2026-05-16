FROM eclipse-temurin:21-jre
RUN useradd -m appuser
WORKDIR /app
COPY novel-admin.jar /app/novel-admin.jar
RUN chown -R appuser:appuser /app
USER appuser
ENV dburl=""
ENV username=""
ENV	password=""
ENV redishost = ""
ENV redisport = ""
ENV redispwd = ""
ENTRYPOINT ["java -Dspring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver -Dspring.datasource.url=${dburl} -Dspring.datasource.username=${username} -Dspring.datasource.password=${password} -Dspring.data.redis.host=${redishost} -Dspring.data.redis.port=${redisport} -Dspring.data.redis.password=${redispwd} -jar /app/novel-admin.jar"]
