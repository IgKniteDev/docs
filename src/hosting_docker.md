# The Docker Way

The first and easiest way of self-hosting IgKnite is by using [Docker](https://docker.com/). For those who don't know, Docker basically uses **containers and images** to virtualize an entire operating system within another. This way, you don't need to worry about your applications failing on other platforms if it works on your own machine. Interesting, right? <br>

## Getting familiar

Previously, we ran a command to open and list all the files within IgKnite's directory. Let's run the command again in a new terminal window if you have closed the previous one:

```bash
# Open and list all the files.
$ cd IgKnite && ls
```

Notice something? Even if you don't, most Docker uses have already noticed a `Dockerfile` within the directory. This file works as a blueprint for building Docker images. <br>

## Preparing

This time, your very first step will be to install [Docker](https://docker.com/) onto your computer. If you are a developer or a DevOps engineer, there's a high probability that you already have it :P

Once installed, open it and follow along with the additional setup procedures thrown by the app. This would be a great time to learn about Docker by watching [this 100-seconds video](https://www.youtube.com/watch?v=gAkwW2tuIqE&t=338s) made by Fireship if you already don't use this awesome tool as a developer.

You'll also need [Docker Compose](https://docs.docker.com/compose/) to run IgKnite. For Windows and macOS, it comes bundled with the original Docker package. However, you'll have to install it separately on Linux distributions. <br>

## Building

Run the docker daemon and then type the following command in your terminal:

```bash
# building the image
$ docker-compose build

# running it
$ docker-compose up

# list running containers
$ docker ps --all
```

## Enjoy!

You should now see logs appearing on your terminal window, eventually displaying the total number of shards and servers IgKnite is connected to. This means you've officially self-hosted IgKnite with Docker!
