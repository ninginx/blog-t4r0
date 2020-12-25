#docker image build -f ./Dockerfile.python.playground -t python3.9-buster --no-cache=true
FROM node:lts-buster-slim

ENV APP_HOME /app
WORKDIR $APP_HOME

RUN apt-get update && apt-get install -y --no-install-recommends curl git apt-utils build-essential apt-transport-https ca-certificates
RUN update-ca-certificates
RUN yarn add global gatsby-cli
COPY . .

ENV PORT 3000

ENTRYPOINT ["tail","-f","/dev/null"]
