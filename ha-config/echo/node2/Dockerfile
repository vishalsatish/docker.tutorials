FROM kaazing/enterprise-gateway:latest

# Generate Keystore entry for kaazing.example.com

RUN keytool -genkeypair -keystore conf/keystore.db -storetype JCEKS -keypass ab987c -storepass ab987c -alias kaazing.example.com -keyalg RSA -dname "CN=kaazing.example.com, OU=Example, O=Example, L=Mountain View, ST=California, C=US"

RUN  curl -L --insecure `curl -sL https://github.com/kaazing/javascript.client.tutorials/releases/latest | grep -i websocket-echo-tutorial.zip | cut -d '"' -f 2 -` -o ./web/websocket-echo-tutorial.zip
RUN  unzip ./web/websocket-echo-tutorial.zip -d ./web

# Add gateway config
COPY node2-config.xml conf/gateway-config.xml
COPY log4j-node2-config.xml conf/log4j-config.xml