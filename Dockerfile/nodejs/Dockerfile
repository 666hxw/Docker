# create a blank image 
from ubuntu  

# install wget
RUN apt-get update \
  && apt-get -y upgrade \
  && apt-get install -y build-essential wget gcc make python

# define nodejs version
ENV NODE_VERSION 8.0.0

# install nodejs
RUN cd /tmp \
    && wget http://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.gz \
    && tar xvzf node-v$NODE_VERSION.tar.gz \
    && rm -f node-v$NODE_VERSION.tar.gz \
    && cd node-v$NODE_VERSION \
    && ./configure \
    && make \
    && make install \
    && cd /tmp \
    && rm -rf /tmp/node-v$NODE_VERSION \
    && npm install -g npm \
    && printf '\n# Nodejs\nexport PATH="node_modules/.bin:$PATH"' >> /root/.bashrc

CMD ["bash"]
 
 
