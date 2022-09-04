# tips

Nginx

Syntax: 	client_header_timeout time;
Default: 	client_header_timeout 60s;
Context: 	http, server

Defines a timeout for reading client request header. If a client does not transmit the entire header within this time, the request is terminated with the 408 (Request Time-out) error.

Syntax: 	client_max_body_size size;
Default: 	client_max_body_size 1m;
Context: 	http, server, location

Sets the maximum allowed size of the client request body. If the size in a request exceeds the configured value, the 413 (Request Entity Too Large) error is returned to the client. Please be aware that browsers cannot correctly display this error. Setting size to 0 disables checking of client request body size.

Syntax: 	client_body_timeout time;
Default: 	client_body_timeout 60s;
Context: 	http, server, location

Defines a timeout for reading client request body. The timeout is set only for a period between two successive read operations, not for the transmission of the whole request body. If a client does not transmit anything within this time, the request is terminated with the 408 (Request Time-out) error.
