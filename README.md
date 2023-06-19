# machine_learning_trading_bot
Machine Learning Trading Bot
The objective is to enhance the existing trading signals with machine learning algorithms that can adapt to new data.

## Tasks
- Establish a Baseline Performance
- Tune the Baseline Trading Algorithm
- Evaluate a New Machine Learning Classifier
- Create an Evaluation Report

## Establish a Baseline Performance
Per the plot below, the baseline plot shows that the actual return is better than the  strategy return. The model needs tuning to get a better performance.

<img src="Delta_[Strategy - Actual]_Baseline.png">

## Tune the Baseline Trading Algorithm 
1. Tune the training algorithm by adjusting the size of the training dataset
- Increasing the training  window decreases the performance of the model
- Performance for 6 months training data
<img src="Delta_[Strategy - Actual]_dataset_6months.png">

  - Decreasing the training window increases the performance of the model
  - Performance for 1 months training data
<img src="Delta_[Strategy - Actual]_dataset_1month.png">

2. Tune the trading algorithm by adjusting the SMA input features.
- Increasing the short SMA window to 20 while keeping long SMA to 100 increases the trading performance compared to the baseline:
<img src="Delta_[Strategy - Actual]_dataset_short20.png">

- Decreasing the long SMA to 50 while keeping short SMA to 4 slightly increases the trading performance compared to the baseline.

<img src="Delta_[Strategy - Actual]_dataset_long50.png">

3. Choose the set of parameters that best improved the trading algorithm returns

From the tuning plot below, it appears that all the strategies are worst than the actual. Among the strategies, keeping the baseline values and only changing the training dataset to 6 months improves the trading algorithms the best.
<img src="Delta_[Strategy - Actual]_tuning_results.png">

## Evaluate Stochastic Gradient Descent
1. Using the baseline parameters, the new SGD ML strategy returns are worst than the actual returns.

<img src="Delta_[Strategy - Actual]_SGD.png">

2. It appears that the SGD model improves the trading strategy in a similar way as the best performer of the SVC parameter tuning cases i.e. changing the SVC  training dataset to 6 months. See the plot below

<img src="Delta_[Strategy - Actual]_SVC_vs_SGD.png">