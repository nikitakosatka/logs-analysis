# logs-analysis

## NASA logs analysis

A program has been developed that analyzes server logs according to this template
```$remote_addr - - [$local_time] “$request” $status $bytes_send```.

The program issues all requests from the logs of this file, which ended with a 5xx error
with the number of unsuccessful requests. Also, using an additional
command-line argument, the program displays a time window when the number of requests to the
server was maximum, and line numbers in the log file.
The functions of the standard C library were used for string parsing. Line
separated by the quotation mark to get the request and response in the next few
characters.


An example of the program's operation with the output of a time window lasting 1 second
(first, the output of the time window, after – all requests that ended with a 5xx error)

![example](https://github.com/nikitakosatka/logs-analysis/blob/main/demo/Screenshot%20at%20Jul%2013%2022-34-06.png?raw=true)
