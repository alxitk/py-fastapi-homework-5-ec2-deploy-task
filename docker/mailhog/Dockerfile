FROM golang:1.24-bookworm


RUN apt-get update && apt-get install -y wget dos2unix && apt-get clean


RUN go install github.com/mailhog/MailHog@latest


ENV PATH="/root/go/bin:$PATH"


COPY commands/setup_mailhog_auth.sh /commands/setup_mailhog_auth.sh

RUN dos2unix /commands/setup_mailhog_auth.sh && chmod +x /commands/setup_mailhog_auth.sh