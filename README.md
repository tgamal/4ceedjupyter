# 4Ceed-Jupyter
4CeeD Jupyter is a data analytics engine for 4Ceed framework. For more information about 4Ceed framework, visit 4CeeD's website at https://4ceed.github.io. This repository extends 4Ceed framework and provide the following features:

* Spawns and manages a [Jupyter notebook](https://jupyter-notebook.readthedocs.io/en/latest/) server for each 4Ceed user 
* Provides a GUI library (Py4Ceed) to select which data to move from 4Ceed to Jupyter 
* Automatically saves new/modified notebooks to 4ceed on termination of the Jupyter notebook server

# Prerequisites
- [Docker](https://www.docker.com/community-edition#/download)
- [Docker Compose](https://docs.docker.com/compose/install/) 


# Setup 4CeeD-Jupyter

*Note: The following commands are run under the project's root directory.*

The `docker-compose`'s definitionsis located in `docker-compose.yml` file. Update `docker-compose.yml` with your own configuration information (e.g., `ADMIN_EMAIL`, `SMTP_SERVER`, etc.) before startup.

To start 4CeeD-Jupyter Framework, simply run the following command:

```
docker-compose pull && docker-compose up
```

or in detached mode:

```
docker-compose pull && docker-compose up -d
```

After all services have been started, 4CeeD's curator is accessible at `http://[MACHINE_IP]:9000/`, where `[MACHINE_IP]` is the IP address of the machine on which `docker-compose` runs. Normally, this IP address can be obtained by running command `ifconfig` on Linux & Mac, or `ipconfig` on Windows. For extractors to work properly, please DO NOT use `127.0.0.1` or `localhost` as IP address for 4CeeD. 

To stop all services, simply press `Ctrl+C`, or run `docker-compose down` if running in detached mode.

%# Testing Jupyter


%1. In the homepage, click on the tab named "Jupyter Session" in the left side of the screen 

%2. Enter a name for the Jupyter session and the duration that you will use the Jupyter notebook server and click on the reserve button

%3. The reserve button will display a link for the Jupyter notebook server. When you click on it, it will show the Jupyter notebook interface.

%4. The notebook has some examples stored in it and you can also see some examples [here](example-notebooks)


# Example Notebook
An example notebook can be found [here](example-notebooks/plot_metadata.ipynb)
