# Rate-limit-kong
Kong Gateway supports the Go language with the go-pdk, a library that provides Go functions to access Kong Gateway features of the PDK. <br>

# Kong install:

```
docker run -d --name kong-dbless --network=kong-net -v "$(pwd):/kong/declarative/" -e "KONG_DATABASE=off" -e "KONG_DECLARATIVE_CONFIG=/kong/declarative/kong.yml" -e "KONG_PROXY_ACCESS_LOG=/dev/stdout" -e "KONG_ADMIN_ACCESS_LOG=/dev/stdout" -e "KONG_PROXY_ERROR_LOG=/dev/stderr" -e "KONG_ADMIN_ERROR_LOG=/dev/stderr" -e "KONG_ADMIN_LISTEN=0.0.0.0:8001" -e "KONG_ADMIN_GUI_URL=http://localhost:8002" -p 8000:8000 -p 8443:8443 -p 8001:8001 -p 8444:8444 -p 8002:8002 -p 8445:8445 -p 8003:8003 -p 8004:8004 kong/kong-gateway:2.7.1.2-alpine
```

# Go kong PDK:
```
go mod init
go get github.com/Kong/go-pdk
go build
```
# Run the project
```
docker-compose up --build
```
