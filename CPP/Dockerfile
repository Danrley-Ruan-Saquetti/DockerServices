FROM gcc:latest

RUN apt-get update && \
  apt-get install -y --no-install-recommends \
  build-essential cmake && \
  apt-get clean && \
  rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY . .

RUN mkdir -p build

WORKDIR /app/build
RUN cmake ../

WORKDIR /app
COPY src ./src

CMD ["bash", "-c", "cd build && make && ./build/program"]