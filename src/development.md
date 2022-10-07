# Development Setup

For those who'd like to add new features to IgKnite using code, low-code or even non-code contributions, this is the perfect chapter to follow along. <br>

## Preparation

The [**preparation for hosting**](./hosting_preparation.md) sub-chapter discusses the primary ways to self-host IgKnite on your local machine. Make sure to read and apply the contents of it properly and then continue reading towards the [**manual hosting**](./hosting_manual.md) sub-chapter as well to set up all of the necessary dependencies. <br>

## Code Style

This project uses the [flake8](https://flake8.pycqa.org) linter for Python and necessary configuration files have also been set up within the repository to support it. [GitHub Actions](https://github.com/features/actions) workflows have been added as well to enforce development with it. 

Setting up the linter is as easy as just running one command:

```bash
# installation
$ python3 -m pip install flake8

# running
$ python3 -m flake8 .
```