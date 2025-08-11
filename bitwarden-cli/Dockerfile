FROM ubuntu:24.04 AS base

WORKDIR /app

RUN apt-get update && apt-get install curl unzip -y

RUN curl -LO https://github.com/bitwarden/cli/releases/download/v1.22.1/bw-linux-1.22.1.zip && \
    unzip bw-linux-1.22.1.zip

FROM ubuntu:24.04 AS runner

COPY --from=base --chmod=0770 /app/bw /usr/bin/bw