MAKE := $(shell which make) -j
DOCKER_COMPOSE := $(shell which docker-compose)
DOCKER := $(shell which docker)

up:
	$(DOCKER_COMPOSE) up -d --build

setup: up
	$(DOCKER_COMPOSE) run --rm web bash -c 'make setup'
	$(MAKE) install

install:
	$(DOCKER_COMPOSE) run --rm web bash -c 'make install'

clean:
	$(DOCKER_COMPOSE) rm -f web

bash/web:
	$(DOCKER) exec -it 1_web_1 bash
