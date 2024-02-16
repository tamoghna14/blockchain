
# Blockchain Implementation in Go

This is a basic blockchain implementation written in Go. It allows for the creation of blocks containing information about book checkouts and provides endpoints to interact with the blockchain via HTTP requests.

## Features

- **Blockchain**: Implements a basic blockchain structure consisting of blocks with hashed data and a linked list structure.
- **HTTP Endpoints**: Provides HTTP endpoints to interact with the blockchain, including adding new blocks and retrieving the entire blockchain.
- **Block Validation**: Ensures the integrity of the blockchain by validating each new block against the previous one.
- **Genesis Block**: Automatically creates a genesis block to initiate the blockchain.
- **Book Data Handling**: Allows for the addition of new books to the system, generating unique identifiers based on book information.

## Requirements

- Go 1.14 or higher
- Gorilla Mux (for routing HTTP requests)

## Usage

1. Clone the repository:

   ```bash
   [git clone <repository-url>](https://github.com/tamoghna14/blockchain.git)
   ```

2. Install dependencies:

   ```bash
   go mod tidy
   ```

3. Run the application:

   ```bash
   go run main.go
   ```

4. Interact with the blockchain using the provided HTTP endpoints.

## HTTP Endpoints

- `GET /`: Retrieves the entire blockchain.
- `POST /`: Adds a new block to the blockchain with book checkout information.
- `POST /new`: Adds a new book to the system with book details.

## Example Usage

1. Add a new book:

   ```bash
   curl -X POST -H "Content-Type: application/json" -d '{"title":"Example Book","author":"John Doe","publish_date":"2023-01-01","isbn":"978-3-16-148410-0"}' http://localhost:3000/new
   ```

2. Write a new block with checkout information:

   ```bash
   curl -X POST -H "Content-Type: application/json" -d '{"book_id":"<book-id>","user":"Alice","checkout_date":"2024-02-16"}' http://localhost:3000
   ```

3. Retrieve the blockchain:

   ```bash
   curl http://localhost:3000
   ```

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, feel free to open an issue or create a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Feel free to modify the README.md file according to your specific project needs and preferences.
