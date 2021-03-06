# 27 March 2018
* updated requirements.txt
* in the wake of recent abuse of datascience tools: ***DO NO EVIL!***

# 19 March 2018
* updated ```requiremnets.txt```
* fixed ```inst_julia.sh```

# 15 March 2018
* added note to the end of ```README.md``` on how to stop the server if launched on boot

# 14 March 2018
* closed  issue #17
* added the solution as an option to ```README.md``` as this might be useful to some

# 12 March 2018
* removed necessity to reboot after changing ```swap_size``` by stopping and starting the service
* updated ```requirements.txt``` 

# 11 March 2018
* closed issues #15 and #16
* issue #15 is personal preference - I may pick up on this at a later stage
* issue #16 is fixed by installing ```nodejs``` with a separate script. For further info please refer to the issue itself
* cut down Julia installation as the JuliaBerry packages lead to segmentation faults
* simplified TeX installtion as suggested in the documentation of ```nbconvert```

# 22 February 2018
* updated requirements.txt
* manually installed the bokeh jupyter lab extension for testing by running: ```jupyter labextension install jupyterlab_bokeh``` Took some time to build but seems to work fine

# 21 Febuary 2017
* updated requirements.txt  

# 17 February 2017
* updated requirements.txt
* it is really amazing how quickly updated packages become available on piwheels...

# 14 February 2018
* HAPPY VALENTINE'S DAY
* updated requirements.txt 

# 10 February 2018
* updated requirements.txt
* if you installed prior to this update, just run:

```bash
source /home/pi/.venv/jns/bin/activate
pip list --outdated --format='legacy'
pip install -U package1 package2...
```
where ```package1 package2...``` is a list of package names of the packages you want to update
 

# 26 January 2018
* added support for Sphinx for new installations 
* in case you want to add this manually because you already have a working jns installation  just run:

```bash
sudo apt install latexmk
source ~/.venv/jns/bin/activate
pip3 install Sphinx docutils 
```

# 24 January 2018
* corrected `inst_jns.sh` and corresponding entry in `README.md`


# 22 January 2018
* set size of swap_file to 2048MB


# 21 January 2018
* modified `conf_jupyter.sh`in order to facilitate use of `ipywidgets` and `bqplot` in JupyterLab


# 20 January 2018
* new version on GitHub


# 15 January 2018
## IMPORTANT NOTIFICATION: I plan to release a new version of jns within this week

***KEY CHANGES***
* Rather than installing the latest version of Python, the new version will use the latest Python 3 version supported in Raspbian - as of this writing Python 3.5.3.
* Whilst this seems to be a step backwards, it is a in fact a giant step forward as we benefit from significant installation speedups made possible by the recently released  ***piwheels*** project.
* The scripts will work across the entire range of Raspberry Pis - perhaps with the exception of the early models with just 256MB of memory - I tested Pi 1, 2, 3 and ZeroW.
* The new version provides Python support for gpio, sensehat and picamera without the worries of breaking things on the system level as all Python modules will be pip installed into a virtual environment using a requirements.txt file.
* This achieves a more maintainable setup and opens up more possibilities.
* Pyhon 3, Julia and Bash kernels will be installed and configured. R, Ruby and Octave kernels are likely to follow as I find the time.
* JupyterLab will be installed and ready to use.

