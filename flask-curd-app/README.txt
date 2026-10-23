create user
------------
curl -s -X POST localhost:5000/api/users \
  -H "Content-Type: application/json" \
  -d '{"name": "Alice", "email": "alice@example.com"}' | jq

verify user 
------------
curl -s localhost:5000/api/users
curl -s localhost:5000/api/users/$ID | jq

put user
--------
curl -s -X PUT localhost:5000/api/users/$ID \
  -H "Content-Type: application/json" \
  -d '{"name":"Alice Smith"}' | jq

delete user 
----------
curl -s -X DELETE localhost:5000/api/users/$ID | jq 
