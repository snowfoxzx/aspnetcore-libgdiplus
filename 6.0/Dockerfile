FROM mcr.microsoft.com/dotnet/aspnet:6.0

LABEL "org.opencontainers.image.authors"="snowfoxzx" \
      "org.opencontainers.image.title"="ASP.NET Core runtime - libgdiplus" \
      "org.opencontainers.image.description"="ASP.NET Core runtime with libgdiplus & libpangocairo." \
      "org.opencontainers.image.source"="https://github.com/snowfoxzx/aspnetcore-libgdiplus" \
      "org.opencontainers.image.base.name"="mcr.microsoft.com/dotnet/aspnet:6.0"

#RUN set -x; buildDeps='git libgif-dev autoconf libtool automake build-essential gettext libglib2.0-dev libcairo2-dev libtiff-dev libexif-dev' \
#    && runDeps='libpangocairo-1.0-0' \
#    && buildDir='/usr/src/libgdiplus' \
#    && apt update \
#    && apt install -y $buildDeps $runDeps \
#    && mkdir -p $buildDir \
#    && git clone https://github.com/mono/libgdiplus.git $buildDir \
#    && cd $buildDir \
#    && ./autogen.sh \
#    && make \
#    && make install \
#    && cd \
#    && rm -rf /var/lib/apt/lists/* \
#    && rm -r $buildDir \
#    && apt purge -y --auto-remove $buildDeps

RUN set -x; runDeps='libgdiplus libpangocairo-1.0-0' && \
    apt update && \
    apt install -y --no-install-recommends $runDeps && \
    rm -rf /var/lib/apt/lists/*
