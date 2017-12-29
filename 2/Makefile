MAKE := $(shell which make) -j
DOCKER_COMPOSE := $(shell which docker-compose)
DOCKER := $(shell which docker)
GIT := $(shell which git)

up:
	$(DOCKER_COMPOSE) up -d --build

setup: up
	$(DOCKER_COMPOSE) exec web bash -c 'make setup'

run:
	$(DOCKER_COMPOSE) exec web bash -c 'make run'

clean:
	$(DOCKER_COMPOSE) rm -f web
	sudo rm -rf web/my-app

bash/web:
	$(DOCKER) exec -it 2_web_1 bash

change-owner:
	sudo chown -R ${USER} web/my-app
