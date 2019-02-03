# web-syslog

You can try to generate websocket for this html like this:

  (echo -e 'HTTP/1.1 200 OK\nAccess-Control-Allow-Origin: *\nContent-type: text/event-stream\n' && tail -f /var/log/syslog | sed -u -e 's/^/data: /;s/$/\n/') | nc -l -k -p 8088
