# The Manual Way

If you're not into [Docker](https://docker.com/) or you'd like to set up IgKnite for coding on it, this is the perfect place to get your hands dirty and run IgKnite with full manual management on the dependencies. <br>

## Preparation

Unlike the Docker setup method, this one requires a fair bit of dependencies to be installed beforehand.

- You will need a [Python](https://www.python.org/downloads/) installation of **version 3.10 or higher.**
- You will need a native installation of [ffmpeg](https://www.python.org/downloads/) for running music commands.

For now we'll only set up these two, but later we'll install more using a package manager. <br>

## Installation

Let's navigate to the directory where IgKnite resides, using the previous command:

```bash
$ cd IgKnite
```

Now that we're in, it's time to set up a [virtual environment]() for Python. Since we don't want to get our hard drives dirty in the process of running the project, we'll use such environments to centralize all of the Python packages inside the directory. <br>

We'll be using the [venv]() shell script provided built-in with Python like this:

```bash
# creating the environment
$ python3 -m venv ourenv

# activating it
$ source ourenv/bin/activate
```

The following command will create a new folder named `ourenv` within IgKnite's project directory. This folder will contain all of the packages and symlinks we need. <br>

Once done, we can install the required Python packages using [pip]():

```bash
# the -r flag specifies a file path
$ python3 -m pip install -r requirements.txt
```

<br>

## Enjoy!

This might take a while, but once all of the installation procedures are complete, we can finally run igKnite using this tiny command right here!

```bash
$ python3 main.py
```