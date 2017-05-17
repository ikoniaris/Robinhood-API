
>   Look at License to see where credit is due, This is a cloned copy of the original creator rohanpai25 with minor customizations



# Robinhood
Python Framework to make trades with Robinhood Private API.
See this [blog post](https://medium.com/@rohanpai25/reversing-robinhood-free-accessible-automated-stock-trading-f40fba1e7d8b).

##Current Features 
- Placing buy orders (`Robinhood.place_buy_order`)
- Placing sell order (`Robinhood.place_sell_order`)
- Quote information (`Robinhood.quote_data`)
- User portfolio data (`Robinhood.portfolios`)
- User positions data (`Robinhood.positions`)
<b>* RedKloud additions</b>
   + Keyring user data is saved via OS key authentication system
   + get watchlist
   + reorganize rh watchlist
   + add to watch rh watchlist
 - Still developing more, as i explore

###How To Install:
    pip install -r requirements.txt
***    
###Converting to Python 3
By default, this module is written in Python 2.  For users who wish to use the module in Python 3, use the following command:
    
    2to3 -w Robinhood.py
***
###How to Use (see [example.py](https://github.com/MeheLLC/Robinhood/blob/master/example.py))

    from Robinhood import Robinhood
    my_trader = Robinhood()
    logged_in = my_trader.login(username="USERNAME HERE", password="PASSWORD HERE")
    stock_instrument = my_trader.instruments("GEVO")[0]
    quote_info = my_trader.quote_data("GEVO")
    buy_order = my_trader.place_buy_order(stock_instrument, 1)
    sell_order = my_trader.place_sell_order(stock_instrument, 1)
***
###Data returned
* Quote data
  + Ask Price
  + Ask Size
  + Bid Price
  + Bid Size
  + Last trade price
  + Previous close
  + Previous close date
  + Adjusted previous close
  + Trading halted
  + Updated at
  + Historical Price
* User portfolio data
  + Adjusted equity previous close
  + Equity
  + Equity previous close
  + Excess margin
  + Extended hours equity
  + Extended hours market value
  + Last core equity
  + Last core market value
  + Market value
  + Order history
  + Dividend history
* User positions data
  + Securities owned
* News
########### 


------------------

# Related

* [robinhood-ruby](https://github.com/rememberlenny/robinhood-ruby) - RubyGem for interacting with Robinhood API
* [robinhood-node](https://github.com/aurbano/robinhood-node) - NodeJS module to make trades with Robinhood Private API
