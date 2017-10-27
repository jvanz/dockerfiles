FROM fedora:26

RUN dnf update -y
RUN dnf install -y git

#install seastar framework
RUN git clone https://github.com/scylladb/seastar.git seastar

WORKDIR /seastar

RUN git submodule update --init --recursive
RUN ./install-dependencies.sh
RUN ./configure.py
RUN ninja

RUN cp /seastar/build/release/seastar.pc /usr/share/pkgconfig

WORKDIR /


CMD ["bash"]
