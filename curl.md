# Example curl commands for testing your server

Replace the IP address in the examples with the IP address of your **load balancer, not your servers!**

Run these commands from your host machine, not your server.

## Testing your frontend

```bash
curl http://143.198.159.36   # server1 IP
```

```bash
curl http://159.223.192.34  # server2 IP
```

## Testing your backend

```bash
curl http://143.198.159.36/hey
```

```bash
curl http://159.223.192.34/hey
```

## Testing your load balancer

```bash
curl http://24.144.70.152
```
```bash
curl -X POST -H "Content-Type: application/json" \
  -d '{"message": "Hello from your server"}' \
  http://24.144.70.152/echo 
```
