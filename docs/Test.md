Test
====

1. See installation guide
1. Run `php bin/console server:start 127.0.0.1:8000`
1. Open http://localhost:8000 in a browser
1. Send curl request to create a poll
   ```bash
   curl -H "Content-Type: application/json" -X POST -d '{"channel_id":"niah6qa", "user_id":"c3a4cqe3", "token":"jsn93w", "command":"/poll", "text":"supper soup salad \"taco and burito\" burger"}' http://localhost:8000/new
   ```
1. Send curl request to vote for an answer
   ```bash
   curl -H "Content-Type: application/json" -X POST -d '{"user_id":"c3a4cqe3", "context": {"action":"vote", "token":"jytdd", "answer":"2"}}' http://localhost:8000/vote
   ```
1. Send curl request to end a poll
   ```bash
   curl -H "Content-Type: application/json" -X POST -d '{"user_id":"c3a4cqe3", "context": {"action":"close", "token":"jytdd", "poll":"1"}}' http://localhost:8000/close
   ```
