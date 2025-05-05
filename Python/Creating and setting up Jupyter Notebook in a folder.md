# 1)  Create a project folder and navigate inside it .

# 2) Create a virtual environment 
```bash 
	python3 -m venv venv
```
This creates a virtual environment in the folder .

# 3) Activate the virtual environment .
```bash 
	source venv/bin/activate
```

# 4) Install the Jupyter Notebook :
```bash 
	pip install notebook
```
If you want to install any other required packages like pandas or numpy then you can do it here .

# 5) Launch the notebook :
```bash
	jupyter notebook --no-browser
```
What this will do is that it will give the link which I can paste on to any browser and open the notebook .

This is done so because if i just launch the jupyter nb using the command " jupyter notebook " then it by jupyter notebook --no-browser opens up in safari and safari does not render jupyter notebook well so we use this command .