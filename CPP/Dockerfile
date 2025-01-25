FROM gcc:latest

RUN apt-get update && apt-get install -y cmake && apt-get clean

WORKDIR /app

COPY . .

RUN mkdir -p build

WORKDIR /app/build
RUN cmake ../

WORKDIR /app
COPY src ./src

CMD ["bash", "-c", "cd build && make && ./build/program"]