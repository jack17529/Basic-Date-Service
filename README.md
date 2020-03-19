# Basic-Date-Service

Made a basic date service with go-kit-CLI using gorilla mux router to get the current date, status of the service and validate a date.

## Running
1. Download the project in your GOPATH.
2. cd inside the folder and run `docker-compose up` using the `docker-compose.yml` file or using `go run hello/cmd/main.go` 

## Architechture

hello/  
|---cmd/  
|------service/  
|----------server.go          Wire the service.  
|----------server_gen.go      Also wire the service.  
|------main.go                Runs the service  
|---pkg/  
|------endpoints/  
|----------endpoint.go        The endpoint logic.  
|----------endpoint_gen.go    This will wire the endpoints.  
|----------middleware.go      Endpoint middleware  
|------http/  
|----------handler.go         Transport logic encode/decode data and gorilla mux request reponse routing of the service.  
|----------handler_gen.go     This will wire the transport.  
|------io/  
|----------io.go              The input output structs.  
|------service/  
|----------middleware.go      The service middleware.  
|----------service.go         Business logic.  


## References
1. https://medium.com/@kujtimii.h/creating-a-todo-app-using-gokit-cli-20f066a58e1
2. https://github.com/GrantZheng/kit
3. https://dev.to/napolux/how-to-write-a-microservice-in-go-with-go-kit-a66
4. https://medium.com/@shijuvar/go-microservices-with-go-kit-introduction-43a757398183
