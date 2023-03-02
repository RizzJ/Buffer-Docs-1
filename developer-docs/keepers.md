---
description: >-
  Keepers are bots that run to open and close the queued and expired trades
  respectively.
---

# Keepers

* The users call the `initiateTrade()` from the router in order to open a trade. This function simply collects the fees from the user and adds the user’s request to the trade queue.
* The keeper listens to these requests and calls the `resolveQueuedTrades()` with one or more trades at a time with the data signed(verified) by the publisher and opens or cancels the trades as per the conditions.
* The keeper also keeps track of all the active options. Whenever an option goes from the active to the expired state the keeper runs the `unlockOptions()` with the data signed(verified) by the publisher and closes it based on the moneyness of the option at the time of expiry.
