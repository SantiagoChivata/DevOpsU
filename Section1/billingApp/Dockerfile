FROM nginx:stable-alpine

# use a volume is mor efficient and speed that filesystem
VOLUME /tmp

RUN rm -rf /usr/share/nginx/html/*

COPY nginx.conf /etc/nginx/nginx.conf
COPY dist/billingApp /usr/share/nginx/html
COPY mime.types /etc/nginx/mime.types

# Install OpenJDK 17
RUN apk --no-cache add openjdk17-jre

# Definition of enviroments for JAVA_HOME
ENV JAVA_HOME=/usr/lib/jvm/java-17-openjdk17
ENV PATH=${JAVA_HOME}/bin:$PATH

# Check installation
RUN java -version

# Install java microservice
ENV JAVA_OPTS=""
ARG JAR_FILE
ADD ${JAR_FILE} app.jar

# copy the init script
COPY appshell.sh appshell.sh

# The ports 7080 for backend-app and 80 for web app
EXPOSE 80 7080

ENTRYPOINT [ "sh", "/appshell.sh" ]