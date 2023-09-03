.PHONY: create_env remove_env activate_env
#################################################################################
# GLOBALS                                                                       #
#################################################################################
SHELL=/bin/bash
PROJECT_NAME = scraping
PROJECT_DIR = $(shell pwd)
CONDA_ROOT=$(shell conda info --root)

#################################################################################
# COMMANDS                                                                      #
#################################################################################

## Set up conda environment and install dependencies
create_env:
		@echo ">>> Creating conda environment."
		conda update -n base -c defaults conda
	 	conda env create --name $(PROJECT_NAME) -f environment.yaml --force
	 	@echo ">>> Activating new conda environment"
	 	source $(CONDA_ROOT)/bin/activate $(PROJECT_NAME)

remove_env:
		@echo ">>> Removing conda environemnt"
		conda remove -n $(PROJECT_NAME) --all
