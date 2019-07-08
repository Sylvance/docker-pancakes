FROM ubuntu

RUN echo "Initiating pandoc download ..."

RUN apt-get update \
    && apt-get install -y wget \
    && rm -rf /var/lib/apt/lists/*

RUN wget https://hackage.haskell.org/package/pandoc-1.17.0.3/pandoc-1.17.0.3.tar.gz \
    && tar xvzf pandoc-1.17.0.3.tar.gz \
    && cd pandoc-1.17.0.3

COPY . /opts/calendar

VOLUME . /opts/calendar

ENTRYPOINT ["/bin/sh"]
