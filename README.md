# stockbot
Alpaca algo stock trading bot

Get recommended buy and strong buy stocks daily from Nasdaq.com and get prices from Yahoo and determine which stocks moved the most the previous day, sort those by largest movers (based on open/close $) and buy those stocks if they are going up. When the stock price goes up enough, or at the end of the market day, sell any purchased stocks.

Trade algo can be set to:

"rating" - uses various Nasdaq.com metrics for stock picks

"lowtomarket" - uses low price to market price 

"moved" - uses which stock moved the most in past week

Buy time can bet set to:

"buyatopen" - buy the stocks when market opens

"buyatclose" - buy the stocks before market closes


## Requirements

Uses Alpaca https://alpaca.markets/ for trading. You will need an account with Alpaca to use stockbot.

Set env vars for Alpaca authentication api keys:

```sh
export APCA_API_KEY_ID=<key_id>
export APCA_API_SECRET_KEY=<secrect_key>
export APCA_API_BASE_URL=url
```

url set to:

https://api.alpaca.markets (for live)

https://paper-api.alpaca.markets (for paper)


Install Alpaca python library:

```sh
pip3 install alpaca-trade-api
```

## How to use

Edit config.py and adjust as needed

```sh
python3 stockbot.py -t <tradealgo> -b <buytime>
```
