FROM veyorokonwsri/trips:latest

# Go to $TRIPS_BASE/src and install TRIPS

RUN git clone https://github.com/wdebeaum/step.git
RUN mv step /vagrant

WORKDIR /vagrant/src

VOLUME /vagrant

RUN cd /vagrant/src && \
  ./configure --with-lisp=sbcl && \
  make clean

# Make extra sure we don't have old compiled lisp files from a previous
# install (some aren't removed with "make clean").
RUN find . -name '*.fasl' -delete && \
  make && \
  make install

ENTRYPOINT ["/bin/bash"]
