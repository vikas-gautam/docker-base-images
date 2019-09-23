FROM rajivnix/debian8-base

ENV NODE_VERSION 8
RUN curl -sL https://deb.nodesource.com/setup_$NODE_VERSION.x | bash -
RUN apt-get install -y nodejs gcc g++ make
RUN curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
RUN apt-get update && apt-get install yarn
