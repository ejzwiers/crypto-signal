# Crypto Signals

### Development state: alpha (There are many bugs and documentation is often lagging)

Crypto Signals is a command line tool that automates your crypto currency Technical Analysis (TA) and trading.

Track over 500 coins across Bittrex, Bitfinex, GDAX, Gemini and more!

Technical Analysis Automated:
* Relative Strength Index (RSI)
* Ichimoku Cloud (Leading Span A, Leading Span B, Conversion Line, Base Line)
* Simple Moving Average
* Exponential Moving Average
* Breakouts / Pumps
* MACD

Alerts:
* SMS via Twilio
* Email
* Slack
* Telegram

Features:
* Modular code for easy trading strategy implementation
* Easy install with Docker

You can build on top of this tool and implement algorithm trading and some machine learning models to experiment with predictive analysis.

Coming Soon:
* Automated buying/selling
* Web Client :)


# How to use (Docker)
* First make sure you have [Docker installed](https://docs.docker.com/engine/installation/)
* Next, to create the docker image run `make build` in the root of the project directory.
* Create a .env file which can be populated with settings in the format of OPTION=value which can be derived from the app/default-config.json file. For example if you want to change the how often it updates add SETTINGS\_UPDATE\_INTERVAL=600
* For lists of values separate them with commas. For instance if you want to use specific symbol pairs they are in the format of base\_currency/quote\_currency (i.e. SETTINGS\_MARKET\_PAIRS=BTC/ETH,BTC/USDT)

## How to run
In the root directory run `docker-compose run app` or `make build && make run --env-file=.env` if you don't have docker-compose.

# How to use (Local)
To install the dependencies for this project, perform the following...
- Ensure you are running python 3.6
- install TA-lib from https://www.ta-lib.org/ for your OS.
- `cd app`
- `pip install numpy==1.14.0`
- `pip install -r requirements.txt`

You can add a secrets.json file to the app directory of your project to customize the configuration, the defaults are in app/default-config.json.

## How to run
Navigate to the app directory in your terminal and run with "python app.py"

# Liability
I am not your financial adviser, nor is this tool. Use this program as an educational tool, and nothing more. None of the contributors to this project are liable for any loses you may incur. Be wise and always do your own research.
