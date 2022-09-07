Steps to reproduce the problem

* Start the containers `docker compose up -d`
* Truncate /etc/resolv.conf inside containers to ensure hostnames are not resolved by docker's built-in dns server (nodenames will still be resolvable thanks to /etc/hosts entries)
* Declare a new stream
* Check the logs for stack traces