FROM ubuntu:noble

WORKDIR /src

RUN apt-get update \
  && apt-get install -y --no-install-recommends ca-certificates curl \
  && rm -rf /var/lib/apt/lists/*

RUN curl -LsSf https://astral.sh/uv/install.sh | env UV_UNMANAGED_INSTALL="/usr/local/bin" sh

# uv로 Python 3.12 설치
RUN uv python install 3.12
RUN uv python list

