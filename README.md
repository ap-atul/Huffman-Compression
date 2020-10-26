# Huffman-Compression
Huffman encoding and decoding with simple Serial and Parallel implementations for CPU and GPU (cuda)


## Algorithm
1. Compression
```
* Read the input data
* Get the frequencies for each symbol
* Build a tree from the frequencies
* Build a dictionary that store which letter has what frequency
* Check the sequence in the dictionary
    * write bits starting from the root node
    * one byte is written to file
* Write the frequency and compressed data to the output file
```

2. De-compression
```
* Read the frequency and compressed data from the file
* Build a tree from the frequencies
* Build a dictionary that store which letter has what frequency
* Check the sequence in the dictionary
    * get letter for the bits
    * get one byte data
* Write the letters to the output file
```

## Execution
1. Clone the repo
```console
$ git clone https://github.com/AP-Atul/Huffman-Compression.git
```
2. Run the makefile for the serial
```console
$ make serial
or
$ make -B serial
```
3. Run the binary files on input file to compress
```console
$ ./bin/compress input.txt input.compressed
```
4. Or decompression
```console
$ ./bin/decompress input.compressed input_decompressed.txt
```

### For parallel with cuda
```console
$ make -B cuda
```
* Compression
```console
$ ./bin/compress_cuda input.txt input.compressed
```
4. Decompression (serial)
```console
$ ./bin/decompress input.compressed input_decompressed.txt
```

## Issues
For any help or problems with the code raise an issue.
    