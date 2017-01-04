# Person-of-Interest-Final-Project
This program will utilize machine learning techniques to train and test an Enron employee data set to determine possible persons of interest with regards to the company's corporate fraud case in 2001

---Project Overview---


---Methodology---
The course presented me with the starter code that processes the data, takes your features of choice, then puts them into a numpy array, which is the input form that most sklearn functions assume. My task was to select the features, pick and tune an algorithm, test, and evaluate your identifier. Several of the mini-projects were designed with this final project in mind, and were compiled accordingly for the final code. The final submission is twofold. First, and most importantly, the final project steps are in a series of focused questions on the Udacity website. Your responses should be about 1 paragraph for each question; taken together, they will be the way that you report to another person (most notably your Udacity coach) what you tried, and what you eventually ended up using as your final analysis strategy. We advise that you keep notes as you work through the project; your thought process is, in many ways, more important than your final project and we will by trying to probe your thought process in these questions. Second, you will create three pickle files (my_dataset.pkl, my_classifier.pkl, my_feature_list.pkl) and turn those in to your Udacity coach when you submit your writeup; your coach will test them using the tester.py script. This step is just to check that you’ve created useable machine learning code, and to verify the performance and parameters of your algorithm. These pickle files are already set up to be made at the end of poi_id.py, you don’t need to add any code to create them. As you are probably already aware, as preprocessing to this project, we've combined the Enron email and financial data into a dictionary, where each key-value pair in the dictionary corresponds to one person. The dictionary key is the person's name, and the value is another dictionary, which contains the names of all the features and their values for that person. The features available to you are the following:

['salary', 'to_messages', 'deferral_payments', 'total_payments', 'loan_advances', 'bonus', 'email_address', 'restricted_stock_deferred', 'deferred_income', 'total_stock_value', 'expenses', 'from_poi_to_this_person', 'exercised_stock_options', 'from_messages', 'other', 'from_this_person_to_poi', 'poi', 'long_term_incentive', 'shared_receipt_with_poi', 'restricted_stock', 'director_fees']

These fall into three major types of features, namely financial features, email features and POI labels.

(1)
financial features:
['salary', 'deferral_payments', 'total_payments', 'loan_advances', 'bonus', 'restricted_stock_deferred', 'deferred_income', 'total_stock_value', 'expenses', 'exercised_stock_options', 'other', 'long_term_incentive', 'restricted_stock', 'director_fees'] (all units are in US dollars)

(2)
email features:
['to_messages', 'email_address', 'from_poi_to_this_person', 'from_messages', 'from_this_person_to_poi', 'poi', 'shared_receipt_with_poi'] (units are generally number of emails messages; notable exception is ‘email_address’, which is a text string)

(3)
POI label:
[‘poi’] (boolean, represented as integer)

As a student, I was encouraged to make, transform or rescale new features from the starter features. I stored the new feature to my_dataset, and used the new feature in the final algorithm, you should also add the feature name to my_feature_list, so your coach can access it during testing. For a concrete example of a new feature that you could add to the dataset, refer to the lesson on Feature Selection.

