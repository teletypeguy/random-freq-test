# Random Freq Test
Some old code for testing a simple random number generator (rng), for generating random-ish sine freqs given session params.  This uses a couple-of-lines linear congruential generator set to return 0 to 100 in a reasonably-uniform distribution, with a sequence length of 800. 

The seed for the pseudo-random sequence can be changed for each session, resulting in different random freq distributions. In the target hardware, we change the seed every time a session is run since it will be fed from a free-running wrap-around counter. The time between power-on and when the RNG is started will vary every time, hence the counter feeding the seed will be effectively-random. This will result in a different random freq sequence (and distribution) every time a session is run.
