# The Manual Way

If you're not into [Docker](https://docker.com/) or you'd like to set up IgKnite for coding on it, this is the perfect place to get your hands dirty and run IgKnite with full manual management on the dependencies. <br>

## Requirements

- The latest [Python](https://www.python.org/downloads/) installation.
- [Poetry](https://python-poetry.org/) for managing Python dependencies.
- A native installation of [ffmpeg](https://www.python.org/downloads/) for running music commands.

For now we'll only set up these two, but later we'll install more using a package manager. <br>

## Installation

Let's navigate to the directory where IgKnite resides, using the previous command:

```bash
$ cd IgKnite
```

Now that we're in, it's time to set up a **virtual environment** for Python. Since we don't want to get our hard drives dirty in the process of running the project, we'll use such environments to centralize all of the Python packages inside the directory. <br>

We'll be using the [venv](https://docs.python.org/3/library/venv.html) command provided built-in with Python like this:

```bash
# creating the environment
$ python3 -m venv venv

# activating it
$ source venv/bin/activate
```

The following command will create a new folder named `venv` within IgKnite's project directory. This folder will contain all of the packages and symlinks we need.
Once done, we can easily install the dependencies using the following command:

```bash
# install using poetry
$ poetry install --sync --no-root
```

<br>

## Enjoy!

This might take a while, but once all of the installation procedures are complete, we can finally run igKnite using this tiny command right here!

```bash
# run the bot
$ python3 main.py
```