# wild-ideas
Some wild ideas running through my head

Combining a few ideas; 

* Modern computer programs are really slow. Too much abstraction, languages and frameworks are based on vibes and hype
* C is the best language for low level programming, however has a lot of floaws. It is inherently single threaded, a bad design. Doesn't take advantage of vector instructions.
  - Look at CUDA; C-like language that has great low level support for parallel programming. Gives programmer a lot of control
  - Look at new C-like language; compare to CUDA, zig, Rust(?)
  - Only support RISCV(?) maybe ARM(?)
  - Simple scripting language on top; doubles as shell
* All modern OSes suck and are bloated
  - All you need is a browser and a terminal
  - can get a cool networking stack
* Cloud hosting pays kind of decent. Something comparable to a $3/month t2.nano is like $30
  - with a super efficient OS, efficient programming language, efficient networking stack and server, can make low cost low power compute as an investment
 
* More fleshed out; use encryption to protect OS source and some processes. Look into understanding some distributed ledger algorithms maybe?
  - check out https://github.com/openfheorg/openfhe-development/tree/main/src/pke/examples for algorithm examples
  - based on this talk sort of, https://chatgpt.com/share/199a66e7-1e72-4a94-8933-a65660218cca
  - need a protocol, was thinking of having custom communication protocol; think of the weaknesses of modern protocols
    * how do you initiate a handshake? maybe just give out a signal asking for people to connect over and over on a fixed frequency with a simple magic character pattern, something that encodes to 'EAT ME' because I'm in an Alice in Wonderland mood
    * to find potential connection, a radio would just do a sweep of the spectrum, this is where something like an sdr is helpful
    * you choose when you want to connect, can always just listen, have a list of trusted servers, etc.
    * every radio would need a serial number; how would you store it? could have a centralized ledger of serial numbers maybe and store trust information there?
    * would the serial number be mutable? how do you prevent it from being stolen?
    * https://chatgpt.com/share/784fcb60-89f2-483b-acc7-e6d057dfc073
    * thought process was to follow design patterns for hardware crypto wallets
