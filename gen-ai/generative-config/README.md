# Generative config

These are not the parameters used to train the LLM, these are addition params used during inference to control the completion.

## Max new tokens

limit the output token cap.

## Sample top K

sampling technique to limit the random sampling and increase the chance of output to be sensible.

config defines the number to tokens (words) to consider.

    prob        word
    0.20        cake        k=1
    0.10        donut       k=2
    0.02        banana      k=3
    0.01        apple
    .
    .
    .

setting k=3 will choose the next word only from cake, donut or banana.

## Sample top P

sampling technique to limit the random sampling and increase the chance of output to be sensible.

config defines the cumulative probability.


    prob        word
    0.20        cake
    0.10        donut
    0.02        banana
    0.01        apple
    .
    .
    .

setting p <= 0.30 will choose the next word only from cake & donut, the total (0.20 + 0.10 = 0.30) probability is limited to 0.30.

## Temperature

higher the temperature the higher the random ness, lower the temperature lower the randomness.

### <1 cooler temperature

Strongly peaked probability distribution

### >1 higher temperature

Broader, flatter probability distribution
