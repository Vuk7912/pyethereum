# Ethereum Utilities Library

## Project Overview

This library provides low-level utility functions and data structures for Ethereum-related operations, with a focus on fundamental blockchain encoding and parsing mechanisms. It implements core components essential for Ethereum protocol interactions, including:

- RLP (Recursive Length Prefix) encoding and decoding
- Transaction parsing and processing
- Trie data structure implementations
- Block and transaction management utilities

### Key Features

- 🔢 RLP encoding/decoding for various data types
- 🔐 Robust binary and integer conversion utilities
- 🧩 Flexible transaction and block processing
- 🌳 Trie data structure implementation

## Installation

### Prerequisites
- Python 2.x (Note: This is an older implementation)
- No external dependencies required

### Package Installation
```bash
# Clone the repository
git clone https://github.com/ethereum/pyethereum.git

# No pip/package manager installation recommended 
# as this appears to be an early/experimental implementation
```

## API Reference

### RLP Module (`rlp.py`)

#### Encoding Functions
- `encode(s)`: Encodes integers, strings, and lists using RLP encoding
  ```python
  rlp.encode(42)  # Encodes an integer
  rlp.encode("hello")  # Encodes a string
  rlp.encode([1, 2, 3])  # Encodes a list
  ```

#### Decoding Functions
- `decode(s)`: Decodes RLP-encoded data
  ```python
  rlp.decode(encoded_data)  # Returns the original data structure
  ```

#### Utility Functions
- `to_binary(n, L=None)`: Converts integer to binary representation
- `from_binary(b)`: Converts binary back to integer
- `binary_length(n)`: Calculates binary length of a number

### Transaction Parsing (`parser.py`)
- `parse(inp)`: Parses transaction data
  ```python
  parser.parse(transaction_input)  # Returns parsed transaction details
  ```

### Other Modules
- `blocks.py`: Block-related utilities
- `transactions.py`: Transaction processing
- `trie.py`: Trie data structure implementation
- `manager.py`: General management utilities

## Repository Structure
```
.
├── rlp.py          # RLP encoding/decoding implementation
├── parser.py       # Transaction parsing utilities
├── blocks.py       # Block-related functions
├── transactions.py # Transaction processing
├── trie.py         # Trie data structure
└── trietest.py     # Trie implementation tests
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

### Running Tests
```bash
# Note: Test running mechanism not explicitly defined
# Recommend checking trietest.py for potential test cases
```

## License

This project is an early Ethereum implementation. Please refer to the original Ethereum repository for licensing details.

**Disclaimer**: This is an experimental/historical implementation. For production use, refer to current Ethereum libraries.