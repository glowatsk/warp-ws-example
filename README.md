### Instructions
Clone the repository.

Run the server with cargo run.

Connect with curl submitting a user id:

```
curl -X POST 'http://localhost:8123/register' -H 'Content-Type: application/json' -d '{ "user_id" : 1 }'

> {"url":"ws://127.0.0.1:8123/ws/8f9a39acba3c4bdd84f2abd7205a6aa3"}
```

Connect to the websocket response url.

Using wscat:

```
wscat -c ws://127.0.0.1:8123/ws/8f9a39acba3c4bdd84f2abd7205a6aa3
```

Can send messages, the server will print them out.
