# Machine Learning Trading Bot Evaluation

## Baseline Algorithm

![Screenshot 2023-09-19 at 8 20 48 PM](https://github.com/br4nders0n/module_14_challenge/assets/133409952/a5f149e8-31e7-48c0-bb8d-a572d1d71a0a)

![Screenshot 2023-09-19 at 8 28 14 PM](https://github.com/br4nders0n/module_14_challenge/assets/133409952/0e9c6b89-85d3-4bb4-bc1b-4cbd7490e735)

When reviewing the classification report of the baseline algorithm, there are several data points to be derived. First, the model has a high recall when buying long of 96% and low recall when selling short of 4%. In turn, the accuracy when buying long was 56% and 43% when selling short. The model does a better job when predicting to buy long.

## Tune the Baseline Algorithm

### What impact resulted from increasing or decreasing the training window?
In this section, I increased the short window from 4 to 10 and decreased the long window from 100 to 50. 

![Screenshot 2023-09-19 at 8 39 46 PM](https://github.com/br4nders0n/module_14_challenge/assets/133409952/c96b9776-5627-489b-8ec4-e3729a7b4a8a)

This increased the buying long recall to 98% from 96%. The accuracy of selling short also fell to 40% from 43%. 

![Screenshot 2023-09-19 at 8 40 40 PM](https://github.com/br4nders0n/module_14_challenge/assets/133409952/21be9bfd-5170-4e9d-8e57-0021cb175634)

As you can see from the graph, the two strategies yield almost the same results until 2020. From 2020 to 2021, the actual returns yield a slightly worse result. 

### What impact resulted from increasing or decreasing either or both of the SMA windows?

In this section, I adjusted the date offset from 3 to 6 months. 

![Screenshot 2023-09-19 at 8 47 44 PM](https://github.com/br4nders0n/module_14_challenge/assets/133409952/fd1c577d-820f-4710-a074-fe0cd3fe503c)

Accuracy of selling short increased by 1% from baseline and recall increased by 2% for buying long. 

![Screenshot 2023-09-19 at 8 48 48 PM](https://github.com/br4nders0n/module_14_challenge/assets/133409952/af2643dc-05ec-4617-847b-8c379b02ac31)

The strategies differ much more than the example above. The strategy returns dip below the actual returns from 2019-2020 and then go above from 2020-2021.

### Choose the set of parameters that best improved the trading algorithm returns

Changing the short window to 5, long window to 25, and date offset to 1. Yielded the following:

![Screenshot 2023-09-19 at 8 58 20 PM](https://github.com/br4nders0n/module_14_challenge/assets/133409952/9f09e410-0ee8-4cfe-9c78-55a9e150159a)

![Screenshot 2023-09-19 at 8 58 44 PM](https://github.com/br4nders0n/module_14_challenge/assets/133409952/58464187-434c-4cf3-ac78-bed14b5ad3fa)

## Evaluate a New Machine Learning Classifier

For this section, I imported the LogisticRegression classifier from SKLearn to backtest the model.The results are as follows:

![Screenshot 2023-09-19 at 9 15 10 PM](https://github.com/br4nders0n/module_14_challenge/assets/133409952/914d287e-3a04-46e7-af8d-996e36e4782b)

![Screenshot 2023-09-19 at 9 15 29 PM](https://github.com/br4nders0n/module_14_challenge/assets/133409952/bd0dcd6d-c9c4-491f-b2dd-c47d1486bea1)

I do not believe that the logistic regression backtest performed well. The model did well compared to the baseline from 2015-2018. From there on, the model did not track to the actual returns. 

## Evaluation Report

In summary, 

