FROM golang:1.20-alpine

WORKDIR /app

# Copy go.mod and go.sum first (optional if go.sum not present)
COPY go.mod ./

# Copy source code
COPY . .

RUN go build -o service1 .

EXPOSE 8001

CMD ["./service1"]
