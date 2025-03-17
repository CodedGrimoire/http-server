# Simple HTTP Server in Rust

This project is a simple HTTP server built using Rust and the `hyper` crate. It can handle basic GET and POST requests, serve static files, and return responses based on request methods.

## Features
- Handles `GET` requests and serves an `index.html` file.
- Handles `POST` requests and echoes the request body.
- Returns `404 Not Found` for unknown paths.
- Returns `405 Method Not Allowed` for unsupported methods.

## Requirements
- Rust (latest stable version recommended)
- Cargo (Rust package manager)

## Installation
Clone the repository and navigate to the project directory:
```sh
git clone https://github.com/yourusername/simple_http_server.git
cd simple_http_server
```

## Running the Server
Use Cargo to build and run the project:
```sh
cargo run
```
The server will start listening on `http://127.0.0.1:3000/`.

## Testing the Server
### 1. Test GET Request
Open a browser or use `curl`:
```sh
curl http://127.0.0.1:3000/
```
If `index.html` exists, it will be served. Otherwise, it will return `File not found`.

### 2. Test POST Request
Send a POST request with some data:
```sh
curl -X POST -d "Hello, Server!" http://127.0.0.1:3000/
```
The server will respond with:
```
Received POST request with body: Hello, Server!
```

## Future Improvements
- Add support for more routes.
- Serve multiple static files.
- Implement logging and error handling.
- Add TLS support for HTTPS.

## License
This project is open-source under the MIT License.

---

