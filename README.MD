# Ocen Huffman Compressor

This is a Huffman compression and decompression tool implemented in Ocen, a programming language created by [Mustafa](https://github.com/mustafaquraish).

## Overview

This program implements the Huffman coding algorithm for lossless data compression. It can both compress and decompress files using Huffman coding.

## Features

- File compression using Huffman coding
- File decompression of Huffman-coded files
- Command-line interface for easy usage
- Supports input from files or standard input
- Can output to files or standard output

## Usage

```
./huffman <-c|-d> -i <input_path> -o <output_path>
```

### Options:

- `-c` or `--compress`: Compress the input file
- `-d` or `--decompress`: Decompress the input file
- `-i <path>` or `--input <path>`: Specify the input file path (default: /dev/stdin)
- `-o <path>` or `--output <path>`: Specify the output file path (default: /dev/stdout)
- `-h` or `--help`: Display help information

## Examples

Compress a file:
```
./huffman -c -i input.txt -o compressed.bin
```

Decompress a file:
```
./huffman -d -i compressed.bin -o decompressed.txt
```

## Implementation Details

The compressor uses the following key components:

1. A `Node` struct to represent elements in the Huffman tree
2. A priority queue (implemented as a min-heap) to build the Huffman tree
3. Bit-level I/O operations for efficient compression and decompression
4. Tree encoding and decoding for storing the Huffman tree structure

## Building

To build the project, you need to have the Ocen compiler installed. Once you have it, you can compile the project using:

```
ocen compressor.oc -o huffman
```


## Acknowledgments

Check out [Ocen](https://github.com/ocen-lang/ocen)