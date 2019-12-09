# Continous Outcomes

Although we don't currently have a vignette on continuous outcomes, here are some instructions. The analysis would be very similar to the one in the vignette for dichotomous data, but with the following modifications: 

- You should prepare your data similarly to dichotomous outcomes but instead of having a column for the number of events you will need a column for the mean and a column for the SD of your outcome. (If you have SE you need to convert it to SD first by multiplying by sqrt(n)).

Then there will be some changes in the arguments of some functions. 

- In net.tab, you will have to change type.outcome="continuous".
- In nma.model, you will have to change family="normal" and link="identity" and set sd = to the name of the column that contains the SD of the outcome. 
- The argument outcome = in nma.model needs to be set to the name of the column that contains the mean of your outcome.
