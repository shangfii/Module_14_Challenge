# Module_14_Challenge
Algorithmic trading

Algorithmic trading uses technical indicators and conditional logic to identify signals for entering and exiting trades. First, we’ll learn how to build a simple trading algorithm. Later in the module, we’ll apply our knowledge of machine learning from earlier modules to evaluate the trading decisions of our algorithm. (We can use machine learning to quickly and efficiently evaluate the performance of trading algorithms.) Understanding how trading algorithms perform on past data offers insight into how they might behave in future market conditions. And, this ultimately leads to better trading decisions, improved portfolio performance, and increased profits.


Tune the Baseline Trading Algorithm



Step 1: Tune the training algorithm by adjusting the size of the training dataset.

What impact resulted from increasing or decreasing the training window?

![3 Month training window](https://github.com/shangfii/Module_14_Challenge/blob/main/SMA4_SMA100_3Months.jpg)


When the training window is decreased to 1 month period, the actual results diverge alot from the strategy results ( See figure with 1 Month training). This could because of under training or not using enough data points to train. 


However, When the training period is increased to 4 months ( similar results at 5 months), we see that the actual results and the trategy results stay very close together for a much longer period of time. So this performs better.

![5 Month training window](https://github.com/shangfii/Module_14_Challenge/blob/main/5_Months_Window.jpg)


If increase to 6 months, then there is a marked divergence again. So the better results are at 4 or 5 months

![6 Month training window](https://github.com/shangfii/Module_14_Challenge/blob/main/6_Months_Window.jpg)



Step 2: Tune the trading algorithm by adjusting the SMA input features.

When we use SMA8 and SMA100 the predictions are really good, the graphs coinside really well, other SMA combinatioins like SMA50 and SMA200 lead to very divergent results between the predicted and the actual. So this is better to use SMA8 and SMA100 since we predict them well

![SMA8 and SMA200](https://github.com/shangfii/Module_14_Challenge/blob/main/SMA8_and_SMA200_with_3_Months.jpg)
![SMA8 and SMA100](https://github.com/shangfii/Module_14_Challenge/blob/main/SMA8_and_SMA100_with_3_Months_training.jpg)


 What impact resulted from increasing or decreasing either or both of the SMA windows?

Step 3: Choose the set of parameters that best improved the trading algorithm returns.

Our best results is when we use SMA8 and SMA100 with a 3 Month training window because that the plots of the actual results and that of the predicted results merge; 

We predict it well using the SVC method, SMA8 and SMA100 with 3 months training This combination also gives an accuracy of 56% the other combinations gives less. We could write another algorithm to plot accuracy vs training period if we want to plot and get the best possible training period, with 3D plots of SMA_slower and SMA_fast with training period we can get the best combination of these three.

The base model gives an accuracy of 56% while the LogisticRegression only gives 52% when we use a training period of 3 and SMA8, SMA100 combination. The base model gives a better accuracy.
