https://www.evanmiller.org/sequential-ab-testing.html
The sequential procedure works like this:

At the beginning of the experiment, choose a sample size N.

Assign subjects randomly to the treatment and control, with 50% probability each.

Track the number of incoming successes from the treatment group. Call this number T.

Track the number of incoming successes from the control group. Call this number C.

If T−C reaches 2N−−√, stop the test. Declare the treatment to be the winner.

If T+C reaches N, stop the test. Declare no winner.

The above procedure can, in some circumstances, reduce the number of observations required for a successful experiment by 50% or more. The procedure works extremely well with low conversion rates (that is, with small Bernoulli parameters). With high conversion rates, it works less well, but in those cases traditional fixed-sample methods should do you just fine.