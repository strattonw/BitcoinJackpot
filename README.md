# BitcoinJackpot
Permanent URL coming soon. Bitcoin clone of [CS:GO Jackpot](https://csgojackpot.com/).

#### What is BitcoinJackpot
We are a Bitcoin based website where you can bet Bitcoins and take the chance to win BIG!

We function in a very simple fashion

* Deposit Bitcoins into your session account
* We give you 1 ticket per 0.0001 bet into the Jackpot
* When 25 bets are received we gather all awarded tickets and randomly pick a winner
* The winner will have their winnings deposited in their BitcoinJackpot session account

##### Rules
* There is no deposit limit per bettor
* There is no limit to the amount of bets a single bettor can make in a single round
* There is a house rake of 5% on every round- this rake is calculated based on the total pool amount in contained within a specific Jackpot round
* Balances are added to the session account after a minimum of 6 blockchain confirmations
* Withdrawls are made instantly on request - all withdrawls carry a 0.0001 minimum amount along with a 0.0001 Miner's Fee

#### Provably Fair
##### What is Provably Fair?
Visit [ProvablyFair.org](http://provablyfair.org/) for more information on Provably Fair

##### BitcoinJackpot Provably Fair

* Round Hash
  * The round hash is an md5 string that is given at the beginning of each round. The hash is generated by concatinating the round winner percentage and the round secret and then applying a md5 encryption on the following string "[ROUND SECRET]-[ROUND WINNER PERCENTAGE]".
* Round Secret
  * The round secret is generated at the beginning of each round but is only displayed at the end of each round. The round secret, along with the round winner percentage, is used to generate the round hash. The round secret is a 48 character alphanumeric string.
* Round Winner Percentage
  * The round winner percentage is used to determine the round winner. To get the winning ticket number the following formula can be applied floor(TotalTickets - 0.0001) * (RoundWinnerPercentage / 100)). After receiving the winner ticket number finding the winning ticket is as simple as counting the number of tickets (1 ticket per 0.0001) starting from bet 1 towards bet 25.