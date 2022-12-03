FROM gcr.io/oss-fuzz-base/base-builder
RUN apt-get update && \
    apt-get install -y make autoconf automake libtool zlib1g-dev

RUN git clone --depth 1 https://github.com/madler/zlib.git
RUN git clone --depth 1 https://github.com/thealberto/libpng-424.git -b fuzzer libpng
RUN cp libpng/contrib/oss-fuzz/build.sh $SRC
COPY build-zlib.sh $SRC/build-zlib.sh
WORKDIR libpng

