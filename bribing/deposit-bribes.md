# Deposit Bribes

The bribes mechanism allows any user to 'bribe' veLE holders to incentivize them to vote for a specific gauge, with the goal of increasing its emissions. Bribes can be deposited during each epoch and will be valid for the subsequent epoch. Each epoch lasts for 7 days, starting at 00:00:00 UTC every Thursday.

\
**Example:**\
\
**-**Collection A wants to increase liquidity in one of their pools. Currently, we are in epoch 7.

\-The Collection A team deposits a bribe in the pool's gauge, which will be available for claiming once epoch 8 begins.

\-If there are no veLE votes in epoch 8, the Collection A team can salvage their rewards by withdrawing them without any penalties.

\-However, if there is at least one vote for the pool's gauge, the bribes will be distributed to each voter based on their vote weight.\
