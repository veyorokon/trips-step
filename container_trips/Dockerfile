FROM veyorokonwsri/trips:latest

# Go to $TRIPS_BASE/src and install TRIPS

COPY ./step /vagrant

WORKDIR /vagrant/src

RUN cd /vagrant/src
RUN ./configure --with-lisp=sbcl
RUN  make clean

# Make extra sure we don't have old compiled lisp files from a previous
# install (some aren't removed with "make clean").
RUN find . -name '*.fasl' -delete
RUN  make
RUN  make install

ENTRYPOINT ["/bin/bash"]
