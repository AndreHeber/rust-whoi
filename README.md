# whoi

`whoi` is a web application built with Rust and the Axum framework. It provides real-time CPU usage data and serves static files.


## Dependencies

The project uses the following dependencies:

- `axum` for web server and routing
- `tokio` for asynchronous runtime
- `sysinfo` for system information
- `serde_json` for JSON serialization
- `comrak` for Markdown parsing

## Getting Started

### Prerequisites

- Rust and Cargo installed. You can install them from [rustup.rs](https://rustup.rs/).

### Building and Running

1. Clone the repository:

    ```sh
    git clone <repository-url>
    cd whoi
    ```

2. Build the project:

    ```sh
    cargo build
    ```

3. Run the project:

    ```sh
    cargo run
    ```

4. Open your browser and navigate to `http://localhost:7032` to see the application.

## Project Details

### `src/main.rs`

The main entry point of the application. It sets up the routes and starts the server.

- `root_get`: Serves the `index.html` file.
- `indexmjs_get`: Serves the `index.mjs` file.
- `indexcss_get`: Serves the `index.css` file.
- `realtime_cpus_get`: Upgrades to a WebSocket connection and streams real-time CPU usage data.

### `src/index.html`

The main HTML file that includes the JavaScript and CSS files.

### `src/index.mjs`

The JavaScript module that handles the WebSocket connection and updates the CPU usage data on the webpage.

### `src/index.css`

The CSS file for styling the webpage.

## License

This project is licensed under the MIT License.
