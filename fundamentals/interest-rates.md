# Interest Rates

There are two different interest rates in the leNFT protocol. The **borrow rate** and the **supply rate**.

### Borrow rate

A reserve's borrow rate (BR) is a function of a its utilization rate (UR). It is designed to keep the reserve's UR around the optimum utilization rate of **70%**. Loans are fixed-rate and use the borrow rate of the reserve at the moment of creation.

![Loan Borrow Rate as a function of a reserve's utilization rate.](../.gitbook/assets/interest\_rate.png)

### Supply Rate

The supply rate is the annual rate at which the deposited assets in a reserve are increasing in value. It depends on the UR of the reserve and the borrow rate of the loans created using it.
