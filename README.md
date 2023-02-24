# Downloader
A multithreaded HTTP file downloader that will resume downloads upon disconnect errors.

Achieves up to 3x download speed efficiency compared to other methods of download (browser, curl, etc), with much better stability.

Has a small amount of machine learning built-in, which will adjust the amount of threads used based on the speeds of previous downloads.

Visualises the download's progress as a bar of chunks that fill up individually based on that chunk's independent progress.

Currently requires the `requests` python package as a dependency for uploading.

## Usage
The last argument (name of output file) is optional, and will be automatically determined if not provided (this will put the file in a folder named `files`). If the URL is not provided, the user will be prompted to input one after the program starts. And finally, if the `-threads x` arguments are not provided, it will automatically be determined based on the file's size as well as the speed of previously downloaded files if applicable.

Additionally, the `-v` (verbose) flag will cause the progress bar to move downwards instead of overwriting itself.
### Windows
`python downloader.py -threads 12 http://speedcheck.cdn.on.net/1000meg.test file.bin`

`py downloader.py http://speedcheck.cdn.on.net/1000meg.test`
### Linux
`python3 downloader.py -threads 12 http://speedcheck.cdn.on.net/1000meg.test file.bin`

`python3 downloader.py http://speedcheck.cdn.on.net/1000meg.test`

### Uploading
The `-u` flag will instead attempt to upload a file to https://mizabot.xyz/files, where it will be stored for an indefinite amount of time. The program will output a link to the file's hosting page once complete. Use this if your file is too large for your browser to handle!
