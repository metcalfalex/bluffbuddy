# bluffbuddy
web page to calculate probabilities for the game Bluff

1. python local web server
2. build base page
3. build dummy javascript
4. aws web server
5. build actual javascript

## Python local web server

cd ~/git/bluffbuddy  
python2.7 -m SimpleHTTPServer  
0.0.0.0:8000

## Base page



## Algoritm

# input: number of dice bid, number of dice you have, number of unknown dice, number of same-call dice, number of off-call dice
# output: zscore of probability
bluff = function(bid,you,unknown,same,off) {
	u = unknown * 1/6 + same * 1/2 + off * 1/12
	print(u)
	s2 = unknown * 1/6 * 5/6 + same * 1/2 * 1/2 + off * 1/12 * 11/12
	return((u-(bid-you+0.5))/sqrt(s2))
}

bluff(5,0,5,5,5) # 12%


