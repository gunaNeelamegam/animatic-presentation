all: clean build release
PASSWORD=$(PYPI_PASSWORD)
USERNAME=$(PYPI_USERNAME)


clean:
		sudo rm -rf dist/ build/ revealjs.egg-info/  
		sudo rm -rf /home/guna/.local/bin/reveal_js 
		sudo rm -rf /usr/local/bin/reveal_js 
		sudo rm -rf /usr/local/lib/python3.8/dist-packages/revealjs-0.1-py3.8.egg
		echo "clean successfully ..........."

build:	
		sudo python3 setup.py install bdist_wheel sdist
		echo "Build Successfully .............."

release:
		pip3 install twine
		twine upload -u $(USERNAME) -p $(PASSWORD) --verbose dist/*
		