
FROM launcher.gcr.io/google/debian9:latest

RUN apt-get update && \
  apt-get install -y unzip curl

RUN curl -sL -o protoc.zip https://github.com/google/protobuf/releases/download/v3.11.4/protoc-3.11.4-linux-x86_64.zip && \
  unzip protoc.zip -d /opt/protobuf && \
  rm protoc.zip && \
  chmod -R 0777 /opt/protobuf

RUN curl -L https://github.com/altipla-consulting/protoc-gen-grpc_browser/releases/download/v0.4.2/protoc-gen-grpc_browser_v0.4.2_linux_amd64 -o /usr/bin/protoc-gen-grpc_browser && \
  chmod +x /usr/bin/protoc-gen-grpc_browser

ENV PATH $PATH:/opt/protobuf/bin
WORKDIR /workspace
