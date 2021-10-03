FROM golang:1.17 AS builder
WORKDIR /src/
COPY . .
RUN go build -o ./bin/

FROM scratch AS final
WORKDIR /app
COPY --from=builder /src/bin/ .
ENTRYPOINT [ "./desafio-go" ]