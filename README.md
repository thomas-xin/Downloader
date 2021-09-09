# Downloader
A multithreaded HTTP file downloader that will resume downloads upon disconnect errors.
Has a small amount of machine learning built-in, which will adjust the amount of threads used based on the speeds of previous downloads.
Visualises the download's progress as a bar of chunks that fill up individually based on that chunk's independent progress.
Currently requires the `requests` python package as a dependency.

## Usage
### Windows
`py downloader.py https://speed.hetzner.de/1GB.bin file.bin`
### Linux
`python3 downloader.py https://speed.hetzner.de/1GB.bin file.bin`
