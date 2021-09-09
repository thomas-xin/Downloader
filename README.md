# Downloader
A multithreaded HTTP file downloader that will resume downloads upon disconnect errors.

Achieves up to 3x download speed efficiency compared to other methods of download (browser, curl, etc), with much better stability.

Has a small amount of machine learning built-in, which will adjust the amount of threads used based on the speeds of previous downloads.

Visualises the download's progress as a bar of chunks that fill up individually based on that chunk's independent progress.

Currently requires the `requests` python package as a dependency.

## Usage
The last argument (name of output file) is optional, and will be automatically determined if not provided (this will put the file in a folder named `files`). If the URL is not provided, the user will be prompted to input one after the program starts.
### Windows
`py downloader.py https://speed.hetzner.de/1GB.bin file.bin`
### Linux
`python3 downloader.py https://speed.hetzner.de/1GB.bin file.bin`
