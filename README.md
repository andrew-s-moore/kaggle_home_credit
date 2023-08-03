# kaggle_home_credit

### Introduction

This repository will touch on the [Kaggle Home Credit Default Risk Competition](https://www.kaggle.com/competitions/home-credit-default-risk/overview) from 2018. This is a classification based probably where we must help Home Credit, the stakeholder, identify which loan applicants are likely to default. 


The *unique* thing about Home Credit is that they target lending to individuals that lack substantial credit history. This means that normal predictors you might find for loan applications do not exist. By being able to more accurately predict wether or not a potential loan applicant with default, Home Credit can **preserve revenue** by loaning to worthy applicants (there will inherently be an expected drop in revenue if we correctly stop lending to bad applicants) and **grow profit margins** by decreasing the cost of granting loans to unqualified applicants.


### Our Goal

Our team set out to tackle this problem in a very specific way:

1. Review & frame the business problem as it pertains to Home Credit's bottom line (maximizing profit, not necessarily revenue)
2. Explore the data, specifically to determine what may be a significant predictor and what to do with NAs
3. Try out & tune various industry standard classification models
4. Review with Home Credit (Kaggle) to understand how our model impact their bottom line

### Our Solution

We started by cleaning the data. Home Credit provided over 100 columns of data. Some of these columns were not relevant, some of these columns were not impactful, and some of these columns couldn't really be deciphered as to what they were. We had to clean this data and narrow the scope down so that any model would only use relevant data and would not use 100+ variables. Following the data cleaning, the team to moved through various classificaiton models (mainly variations of decision trees) leading us to a gradiant boosted model. With hyperparameter tuning, we were able to achieve a respectable score on kaggle which translates to a positive result for Home Credit. Our solution overweights the prediction to predict more defaults than will actually happen. We'll explore this more further below, but if our model can't be perfect, we would rather over predict defaults than under predict.



### My Contribution

My contributions can be grouped in 4 ways:

- **Feature Exploration** - My team coded in Python and I coded in R. While much of my code was not copy-pasted directly into our final model, I contributed here by designing relevant features from the Home Credit data and then moving this working with the group to include some of this in our Python model. This was necessary as Home Credit did not provide some of the information that is standard in the loan industry. A good example of this would be down payment of the loan and the changes to terms off the back of this. (Yes a loan may be 360 months and be for $500,000; however, if there is a downpayment of $250,000, the size of the loan payments will drastically change.) This required research into the industry to understand what predictors were worth creating.

- **Model implementation** - Once we had cleaned all of the data, I assisted in the actual model building in Python. We used many different models trying to find the best one for Home Credit. We knew going into it that we would likely use some form of gradient boosted decision trees, but we wanted to cover all of our basis. This was very fulfilling in the sense that I had not had much exposure to gradiant boosting, but it seems very popular in the industry right now for decision tree/classificaiton problems due to how light weight it is.

- **Code Cleaning & Troubleshooting** - Spent a fair amount of time reviewing, editing, and tuning various code in our modeling.

- **Writing & Visualizations** - Responsible for a majority of the project writing, presentation outline & visuals, business impact analysis,  



### The Business Value

Home Credit will see two immediate impacts from our model

- **Potential Decrease in Revenue due to lower loan writing** - Our model will over predict defaults which will lead to the model lowering the number of loans that Home Credit writes. While overall this is in Home Credit's best interest, due to the nature of writing fewer loans, revenues may decrease. There may also be hidden decreases in expendetures. As Home Credit writes fewer loans, this takes less operational capacity.

  
- **More accurate loan writing will lead to a stronger profit margin** - Due to our model staying on the conservative side, this lower loan writing and potential lower revenue does in fact lead to a stronger profit margin. A defaulting loan can cost Home Credit the profit from 5, 10, or even 20 successfully written loans. By limiting the losses from bad loans, this will drive an increase in Home Credit's bottom line without having to spend additional resources to expand revenues.



### Difficulties

Personally, one of the greatest difficulties to this process was learning the business. This competition did not have a stakeholder that we could actively work with. Machine learning is only as good as the data that is fed into it. While Home Credit provided a plethora of data, it is always a good idea to connect with SMEs within the business to understand the process, how the data is collected (may be built in bias such as employees filling out fields automatically for customers or not providing all the information available), what hunches the SMEs might have, etc. You will not always have this when modeling, but it certainly helps.

As a group, I can think of two themes that impacted us. First, we did not plan the whole structure before starting. As the project went along, we continually changed things or went backwards in order to progress forward. This was not productive and was a bad use of time. If we had done this before starting, we would have saved hours and hours of time. Second, there was not someone with executive decision. There were last minute decisions made without group input or review that made their way into final submissions and presentations. This caused discussion and I th 


### Takeaways

I have two main takeaways from this project that have forever changed how I will run data projects in the future. 

**1. Spend the time to plan the project front to back before beginning.**
This does not necessarily mean that all decisions must be made prior to beginning, but there should be a concrete road map to follow and any deviation to this road map should be thoroughly discussed before going another direction. This is much more productive and engaging instead of moving piece by piece. When moving step-by-step, I felt like the team had to move backwards to move forwards occasionally.

**2. Invest the time exploring, cleaning, and understanding the data available**
I have always heard jokes, stories, and comments from professionals that data preparation is what data scientists actually do the most. I have never given much credence to these statements but now I fully understand. 

-Results can only be as good as the data is. Good data in, good results out. Bad data in, bad results out.

-Companies don't have neat data. This is the first time I have experienced incomplete or unclean data on a scale of this size. I need to better understand how industry professionals clean this data and I need more practice. 

-Companies don't necessarily have the right data. Meaningful data may need to be engineered from what is available and sometimes, companies may need to begin collecting new data types in order to tackle a problem.

In the impeding age of "AI", I worry that many companies will attempt to integrate AI with terrible data inputs. This will only weaken their business. What many of these companies really need now before AI integration is a metrics framework and a data preparation process. 



