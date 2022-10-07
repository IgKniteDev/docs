# The Docker Way

The first and easiest way of self-hosting IgKnite is by using [Docker](https://docker.com/). For those who don't know, Docker basically uses **containers and images** to virtualize an entire operating system within another. This way, you don't need to worry about your applications failing on other platforms if it works on your own machine. Interesting, right?

<br>

## Getting familiar

Previously, we ran a command to open and list all the files within IgKnite's directory. Let's run the command again in a new terminal window if you have closed the previous one:

```bash
# Open and list all the files.
$ cd IgKnite && ls
```

Notice something? Even if you don't, most Docker uses have already noticed a `Dockerfile` within the directory. This file works as a blueprint for building Docker images.

<br>

## Preparing

This time, your very first step will be to install [Docker](https://docker.com/) onto your computer. If you are a developer or a DevOps engineer, there's a high probability that you already have it :P

Once installed, open it and follow along with the additional setup procedures thrown by the app. This would be a great time to learn about Docker by watching [this 100-seconds video](https://www.youtube.com/watch?v=gAkwW2tuIqE&t=338s) made by Fireship if you already don't use this awesome tool as a developer.

<br>

## Building

Let's prepare a new Docker image for IgKnite. Make sure you restart your terminal and `cd` into IgKnite's directory again. Also make sure that you have a stable internet connection. Then, you can type:

```bash
$ docker build -t igknite .
```

This will create a new Docker image with the `igknite` tag. It might take some time to prepare all the dependencies and install them. Once done, run the image in a container using:

```bash
$ docker run --env-file .env igknite
```

- The `--env-file` flag specifies the path to the `.env` file we had accessed previously. This can vary depending on where you have put the actual file. For example, if the file is in a different subdirectory named `env` then `env/.env` would be the path inside the root directory of the project.
- The tag name is specified using the `igknite` parameter at the end.

<br>

## Enjoy!

If you have followed the given steps correctly, you should see your bot coming online within a few moments of command execution.
