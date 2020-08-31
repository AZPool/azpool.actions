
FROM launcher.gcr.io/google/debian9:latest

RUN apt update && \
  apt install -y curl jq

RUN curl -L -o /opt/protoc-gen-grpc_browser $(curl --silent 'https://api.github.com/repos/altipla-consulting/protoc-gen-grpc_browser/releases/latest' | jq -r '.assets[0].browser_download_url') && \
  chmod +x /opt/protoc-gen-grpc_browser

CMD ["/opt/protoc-gen-grpc_browser"]
