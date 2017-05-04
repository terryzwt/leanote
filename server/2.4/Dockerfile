FROM alpine:3.3
RUN apk --update add curl && \
    curl -L https://nchc.dl.sourceforge.net/project/leanote-bin/2.4/leanote-darwin-amd64-v2.4.bin.tar.gz >> \
    /usr/local/leanote-linux-amd64.tar.gz && \
    apk del --purge curl && \
    rm -rf /var/cache/apk/*

RUN tar -xzvf /usr/local/leanote-linux-amd64.tar.gz -C /usr/local
EXPOSE 9000
WORKDIR  /usr/local/leanote/bin
ENTRYPOINT ["sh","run.sh"]
