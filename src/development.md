# Development Setup

For those who'd like to add new features to IgKnite using code, low-code or even non-code contributions, this is the perfect chapter to follow along. <br>

## Preparation

The [**preparation for hosting**](./hosting_preparation.md) sub-chapter discusses the primary ways to self-host IgKnite on your local machine. Make sure to read and apply the contents of it properly and then continue reading towards the [**manual hosting**](./hosting_manual.md) sub-chapter as well to set up all of the necessary dependencies. <br>

## Code Style

In order to maintain a proper and managed syntax, this project has two different packages:

- [flake8](https://github.com/pycqa/flake8) for linting
- [black](https://github.com/psf/black) for formatting

```bash
# installation
$ python3 -m pip install flake8 black
```

<br>

For those who use [Visual Studio Code](https://code.visualstudio.com/), the project also contains configuration for the [isort](https://github.com/microsoft/vscode-isort) extension for automatically organizing imports on every save.