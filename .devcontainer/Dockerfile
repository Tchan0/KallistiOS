# Stage 1
FROM "ghcr.io/kos-builds/kos-ports-dc:sha-656a397-14.1.0" as build

# Add mkdcdisc
RUN git clone https://gitlab.com/simulant/mkdcdisc /opt/toolchains/dc/mkdcdisc \
    && cd /opt/toolchains/dc/mkdcdisc \
    && meson setup builddir \
    && meson compile -C builddir \
    && cp ./builddir/mkdcdisc /opt/toolchains/dc/bin
