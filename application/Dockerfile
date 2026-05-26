FROM alpine:latest AS builder
WORKDIR /build
COPY demo .
RUN chmod +x demo

FROM scratch
WORKDIR /app
COPY --from=builder /build/demo .
EXPOSE 8080
CMD ["./demo"]
