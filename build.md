
### Commands to Build and Run the Application
Run these commands in your terminal to build and run the `scavenger` application:

1. **Navigate to the project directory:**
    ```sh
    cd path/to/scavenger
    ```

2. **Initialize the Go module if not already done:**
    ```sh
    go mod init scavenger
    ```

3. **Download the necessary dependencies:**
    ```sh
    go mod tidy
    ```

4. **Build the binary and name it `scavenger`:**
    ```sh
    go build -o scavenger .
    ```

5. **Run the compiled binary:**
    ```sh
    ./scavenger --start-url "http://example.com"
    ```

This will compile and run your web scraper with the specified binary name `scavenger`. The code is organized for better readability and maintainability while avoiding the use of full module paths for local package imports.