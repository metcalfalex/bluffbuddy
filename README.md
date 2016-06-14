# bluffbuddy
web page to calculate probabilities for the game Bluff

1. python local web server
2. HTML form
3. algoritm
4. d3.js normal distribution
5. d3.js histograms
6. aws web server

## Python local web server

cd ~/git/bluffbuddy  
python2.7 -m SimpleHTTPServer  
0.0.0.0:8000

Must be connected to internet for jquery to load

## HTML form



## Algoritm

input: number of dice bid, number of dice you have, number of unknown dice, number of same-call dice, number of off-call dice
output: zscore of probability
bluff = function(bid,you,unknown,same,off) {
	u = unknown * 1/6 + same * 1/2 + off * 1/12
	print(u)
	s2 = unknown * 1/6 * 5/6 + same * 1/2 * 1/2 + off * 1/12 * 11/12
	return((u-(bid-you+0.5))/sqrt(s2))
}

bluff(5,0,5,5,5) # 12%

## Plots

Hist: *  
http://bl.ocks.org/mbostock/3048450

Line:  
http://bl.ocks.org/mbostock/3883245

Area:  
http://bl.ocks.org/mbostock/3883195

Normal Distribution: *  
http://bl.ocks.org/phil-pedruco/88cb8a51cdce45f13c7e

Calculating Normal Distribution for plotting:  
http://stackoverflow.com/questions/25375386/how-to-create-a-normal-distribution-normal-distribution-in-d3-js



