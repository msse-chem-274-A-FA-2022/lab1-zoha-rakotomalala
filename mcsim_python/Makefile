
.PHONY: environment remove-env install uninstall test # .PHONY is something we can add when our target dependencies are not files.

MODULE=mcsim
ENVIRONMENT=chem274A_lab1

# First it will remove our environment to make sure to start fresh. Then it will create a new environment using Python 3.9, and 
# install all the libraries we want. 
environment: remove-env
	conda create -n $(ENVIRONMENT) "python=3.9" --yes
	conda install -c conda-forge notebook nbconvert numpy matplotlib pytest-cov pandas --name $(ENVIRONMENT) --yes

# It will remove our environment and all the linked installations.
remove-env:
	conda remove --name $(ENVIRONMENT) --all --yes

# First it will uninstall the packages we have installed, and then install all the packages listed in pyproject.toml.
install: uninstall ## install the package to the active Python's site-packages
	pip install .

#  First it will uninstall the packages we have installed, and then it will install all the packages listed in pyproject.toml
# in development mode.
dev-install: uninstall
	pip install -e .

# It will uninstall the packages of the module mcsim.
uninstall: ## uninstall the package
	pip uninstall --yes $(MODULE)

# It will launch a pytest instance that will test our files, and give us verbose explanations.
test: 
	pytest -v
