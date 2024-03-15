list: # List of tasks
# list all targets, should be improved to not list also .PHONY
	@grep '^[^#[:space:]].*:' Makefile

.PHONY: build
build: # Builds the Golang app
	go build app.go

.PHONY: run
run: # Runs the Golang app
	go run app.go

.PHONY: clean  
clean: # Deletes the Golang app
	rm -f app