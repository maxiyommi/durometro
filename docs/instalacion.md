# Instalación

* Instalar [Python](https://www.python.org).
* Instalar [Git](https://git-scm.com/):
    ``` bash
    sudo apt-get update
    sudo apt install git
    ```
* Ver la versión de Python instalada (por defecto viene instalado en Linux):
    ``` bash
    python3 -V
    ```
* Instalar [pip3](https://www.raspberrypi.org/documentation/linux/software/python.md):
    ``` bash
    sudo apt install python3-pip
    pip3 -V
    ```
* Instalar [virtual env](https://virtualenv.pypa.io/en/latest/). [Otra referencia](https://j2logo.com/virtualenv-pip-librerias-python/) (solo para python 2.x)
    ``` bash
    pip install virtualenv
    ```  
> Desde python 3.3 viene instalado por defecto en las librerias estandars bajo el modulo **venv**

* Crear entorno virtual (solo la primera vez).
    ``` bash
    python -m venv env # crea el entorno virtual
    ```
* Activar entorno virtual (siempre).
    ``` bash
    source env/bin/activate # activa el entorno virtual
    deactivate # desactiva el entorno virtual
    rm -r env # eliminar el entorno virtual
    ```
    
* Instalar librerias en el entorno virtual creado (solo la primera vez, a menos que se actualice).
    ``` bash
    pip install -r requirements.txt 
    ```
* En caso de actualizar librerias (opcional).
    ``` bash
    pip freeze > requirements. txt.
    ```
* Instalar [Jupyter Lab](https://jupyterlab.readthedocs.io/en/stable/index.html), con el entorno virtual activado (opcional).
    ``` bash
    sudo pip3 install setuptools
    sudo apt install libffi-dev
    sudo pip3 install cffi
    pip3 install jupyterlab
    ```	  
* [Activar el entorno virtual](https://janakiev.com/blog/jupyter-virtual-envs/) en jupyter lab (alternativo, investigar).
    ``` bash
    pip install --user ipykernel
    python -m ipykernel install --user --name=myenv
    ```