# IQ Options notebooks

This repository contains output-free Jupyter notebooks for exploring IQ Option OTC data and testing simple strategies.

The companion [IQ Options trading bot](https://github.com/oduonye1992/iq-options-trading-bot) collects the candle data used by these notebooks.

## Safety and privacy

These notebooks are research artifacts, not financial advice or a trading system. They do not place trades automatically. Use demo data only, and never risk money you cannot afford to lose.

Outputs, credentials, account details, screenshots, databases, and model files are not part of this repository. Keep local data and generated results outside Git.

## Use

Install [uv](https://docs.astral.sh/uv/) and run:

~~~bash
uv sync
uv run jupyter lab
~~~

The notebooks look in `data/` by default. To analyze data collected by the companion bot, point `IQ_OPTIONS_DATA_DIR` at that bot's data directory:

~~~bash
IQ_OPTIONS_DATA_DIR=/path/to/iq-options-trading-bot/data uv run jupyter lab
~~~

## Docker

~~~bash
docker build -t iq-options-notebooks .
docker run --rm -it -p 8888:8888 \
  -v "$PWD/data:/workspace/data" \
  iq-options-notebooks
~~~

These notebooks are research artifacts, not financial advice or a trading system. Their results should not be treated as evidence of a reliable market edge.
