# Start with Go installed
FROM golang:1.23-bookworm

WORKDIR /app

# Copy and download Go dependencies
COPY go.mod go.sum ./
RUN go mod download

# Copy the code and build the application
COPY . .
RUN go build -o student-app .

EXPOSE 5001

# Start the compiled application
CMD ["./student-app"]