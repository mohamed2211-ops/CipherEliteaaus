docker run -d \
  --name evolution-api \
  --restart always \
  -p 8080:8080 \
  -e AUTH_API_KEY="my_secret_key_123" \
  -v ~/evolution-instance:/evolution/instance \
  tendermint/evolution-api:v2.0.0
