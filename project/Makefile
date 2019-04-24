PACKAGE_DIR=apigw
DOTENV_TARGET=.env

################
# Entry Points #
################

build: $(DOTENV_TARGET)
	docker-compose run --rm serverless make _build

deploy: $(ENV_RM_REQUIRED) $(DOTENV_TARGET) $(ASSUME_REQUIRED)
	docker-compose run --rm serverless make _deploy

remove: $(DOTENV_TARGET) $(ASSUME_REQUIRED)
	docker-compose run --rm serverless make _remove

shell: $(DOTENV_TARGET)
	docker-compose run --rm serverless bash

##########
# Others #
##########

_build:
	cd $(PACKAGE_DIR) && npm install --force

_deploy:
	cd $(PACKAGE_DIR) && rm -rf .serverless && sls deploy -v

_remove:
	cd $(PACKAGE_DIR) && sls remove -v && rm -rf .serverless

_clean:
	rm -rf $(PACKAGE_DIR)
