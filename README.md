
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Data Science Portfolio</title>
  <link rel="stylesheet" href="styles.css">
  <link rel="stylesheet" type="text/css" href="bootstrap.min.css">
  
</head>
<body>
  <header>
    <nav class="sliding-nav">
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="About.html">About</a></li>
        <li><a href="projects.html">Projects</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </nav>
  </header>
  
  <section id="home">
    <h1>Welcome to My Data Science Portfolio</h1>
    <h3>Discover my projects, skills, and experiences in the field of data science.</h3>
  </section>
  
  <section id="about">
    <h2>About Me</h2>
    <p>My name is Christabel Iyamu, and I am based in Manchester, United Kingdom. I graduated with distinction from the University of Salford, where I did my Masters in Data Science. Before coming to study in the UK, I did my degree in Agricultural economics at the University of Benin, graduated with a first class, and got a job with Interswitch Group, a Fin-Tech company, as a data analyst working in the fraud and dispute team. After 2 years of promotion, I was moved to the application implementation team, where I support the team on application issue resolution and updates as a data analyst. I developed an interest in Data science during my work experience as I worked with management to collect and analyze data to enable them to make informed decisions. These datasets I championed helped the company abate a financial loss of over 25 million naira and implement processes to improve some team tasks to help mitigate future losses. Hence, I decided to do further studies in Data science to enable me to offer more solutions using data insights on an advanced level.</p>
  </section>
  
  <section id="projects">
    <h2>Projects</h2>
    <div class="project">
      
      </div class="project">
  
      <h3>Bank Campaign Prediction</h3>
   
    <p><b>Project Overview:</b></p>
      <p>This project depicts the use of the classification method as a machine learning tool to create a model or solution for curbing the following marketing problems:
        <br>•	Low productivity of campaigns using random selection of contacts.
        <br>•	Prolonged campaigns
       <br> •	High cost of resources in running campaigns
          <p><b>Project Objectives:</b></p>
        Based on the problems listed above the following objectives has been set for this study to resolve these problems:
       <br> 1.	Create a model for bank marketing campaigns to clearly explain and predict successful campaigns by determining whether a contact will sign up for a long-term deposit subscription with the bank.
        <br>2.	Determine the relevant features that is required for a successful campaign to manage time and resources.
        </p>
     <p><b>Dataset:</b></p>
     <p>Dataset was collected from UCI dataset repository with link
        <a href=" https://archive.ics.uci.edu/ml/datasets/bank+marketing"><b>Click here for Dataset</b></a>
        The dataset used in this study is related to the direct marketing campaigns of a Portuguese banking institution.
         <p><b>Data cleaning:</b></p>
        Data Cleaning was conducted using Python, using techniques like normalization of data variables for uniform scale, creation of distribution plots of the data class to check for class imbalance, resampling of the datasets using the over-sampling method to get a balanced class in this study to avoid loss of data in the case of under-sampling (the over-sampling technique produced a better accuracy score for the model), and lastly, feature selection techniques using the recursive feature selection technique were explored in this study to meet business needs.
    </p>
     <p><b>Analytical Technques and Tools:</b></p>
      <p>Data modelling for this study was done using K-Nearest Neighbor(KNN) and Adaboost Classifier(Decision tree base model) using Python and two-class Neural Network using Azure machine learning studio. 
      <p><b>Task/Implementation:</b></p>
    Dataset are divided into train and test splits and Models were fitted to train datasets to predict test dataset and achieve good precision models with good F1 score considering the class imbalance. 
    <br>Model was generated using  KNN algorithm and Adaboost Classifier for both before and after feature selection with different number of features and metric scores .</p>
      <p>One of the business needs of this study is to determine the relevant features that is required for a successful campaign to manage time and resources. Hence, feature selection techniques were applied to the dataset using Recursive Feature Elimination with Cross Validation (RFECV) with 6 steps to remove 6 redundant features using LogisticRegression as extimator since class label is binary(categorical). Also, StratifiedKFold was used as cross validation technique to aid in preserving the percentage of samples for each class since class is imbalanced. 
        <p><b>Results/Outcome:</b></p>  
          The model created was able to predict if customer will subscribe to the campaign with an accuracy score of 84% with Adaboost ensemble learning. The model can help marketing managers and their teams determine productive campaigns based on successful customer subscriptions to long-term deposit packages. Such solution would help improve efficiency of marketing campaigns by identifying the main features that affect campaign success, which translates to improved resource optimization and an improved quality selection process for potential buyers.
          <br> Ideally this model will be beneficial to marketing teams even beyond the banking sector in optimising their marketing campaigns.
    <br>Python Notebook of the full code can be accessed here <a href= "https://colab.research.google.com/drive/1cDr6OlnxnNTse091H_ypcGxGbY0d5Ey4?authuser=1#scrollTo=240cee3e"> <b>Click here to see project notebook</b></a> </p>
 </div>
        
    <div class="project">
      <h3>Sales Promotion Using Association Rule Mining Insights for Online Stores in United Kingdom</h3>
        <p><b>Project Overview:</b></p>
      <p>Association rule is an unsupervised learning method where an algorithm tries to learn data that is not labeled. This study will analyze online sales data particularly for customer orders in United Kingdom which has more records of orders in the dataset being evaluated.  This study would identify important sales insights using exploratory data anaysis, explore possible relationships between products ordered by customers and proffer effective association rules that would guide discount sales promotion for online stores.</p>
      <p><b>Dataset:</b></p>
        <p>To achieve study objective, dataset was collected from UCI data repository (see link below).
        <a href= "https://archive.ics.uci.edu/ml/datasets/online+retail"> <b>Click here for Dataset</b></a>
        The dataset being used is the Online Retail Dataset, which contains transactions made on a UK-based online retail store between the 1st of December 2010 and 9th of December 2011 for Customers all over the world
         <p><b>Data cleaning:</b></p>
            <p>Data preparation techniques were conducted on the dataset as missing values were identified in the description and customer id columns; hence, rows with null values were dropped, reducing the total record of data from 541909 rows to 406829 rows.Furthermore, Invoice number column contains invoice numbers of customer orders that were later cancelled and could be identified with letter “C”. Cancelled orders won’t be needed in this analysis hence rows containing invoice number with a “C” in it were dropped reducing out data records to 397924 rows.In line with preparation of dataset in the required format for the algorithm, items purchased by customers were grouped by invoice number and multiplied the grouped data by quantity of items ordered. Unstack function was used to separate products into columns (each column represents an item) while the invoice number was set as index (each row contains details of products ordered for an invoice number). Further transformation was applied to the table to encode data into zeros and one, which is the required format for the apriori algorithm, hence a function was defined to set all values greater than or equal to one as 1(meaning items were purchased) while items with zero or less be classified as 0(meaning items were not purchased).</p>
     <p><b>Analytical Techniques and Tools:</b></p>
        <p>Exploratory data analysis were conducted using Python visualisation charts and plots, e.g., Seaborn, Matplotlib, etc. Association rule mining can be implemented using python libraries like apyori or mlxtend that contain the apriori function and the association rule function. In this study, the MlXtend library was used. The Apriori algorithm is the most used algorithm for association rule mining. It identifies the most frequent item sets in a transaction data and analyses relationships between the items using key measures: support confidence, and lift. 
        <p><b>Task/Implementation:</b></p>
            To generate a frequent item set, the apriori function imported from the mlxtend library was applied to the prepared dataset that has been unstacked and encoded in the right format and below is the result of the analysis ordered by support in descending order (minimum support was set as 0.03).
       <p><b>Results/Outcome:</b></p> 
Sales exploratory data analysis shows that sales increase towards the end of the year, with a peak in November, which is intuitively plausible as customers shop more in preparation of the festive period (Christmas and a new year). The month of February recorded the lowest number of sales, which makes it a target month for sales promotion to boost sales. The hourly sales chart identifies high sales between 9 am to 3pm with a peak at noon which would inform sales promotion plans to intensify strategies at these times to achieve better sales. Efficient application of sales promotion techniques using these insights tends to improve sales of both peak and non-peak periods.In summeary, Considering the results of analysis done in this study, sales promotion is likely to be more efficient when applied at 12pm during the peak time of sales especially weekdays. Also, rewards for loyalty to top purchasing customers as identified in this study will encourage more orders. Top performing stock codes identified by the study should also be adequately stocked during sales promotion campaign. It is also recommended that Discounts for ROSES REGENCY TEACUP AND SAUCER should be promoted to customers who purchase GREEN REGENCY TEACUP AND SAUCER since the likelihood of buying the consequent is high when antecedent has been purchased. This should apply to other rules generated by the algorithm. 
            <br> Ideally, this model will be beneficial to the sales team, particularly in the retail and e-commerce industries, to drive sales and optimise sales promotion to meet their sales targets.
            <br>Python Notebook for Full code can be seen using this link <a href= "https://colab.research.google.com/drive/19d9X6CnpVEDHPg6Nnv96N_XDtxImToAk?authuser=1"> <b>Click here to view project codes</b></a>
    </div>
    <div class="project">
        <h3>Sentiment Analysis and Text Mining for Sampled Hotel Restaurant and Bars Based on Lowest Reviews.</h3>
           <p><b>Project Overview:</b></p>
        <p>In this project, we would analyse a group of 30 least reviewed hotels in our dataset, narrow down to a specific hotel based on percentage of negative reviews identified and conduct sentiment analysis of hotel reviews for selected hotel to find out why reviews were low. This study will create word cloud that presents the most frequent words that customers use in their reviews and visualize the resulting reports using Bar plots, frequency plots and tables.</p>
         <p><b>Data cleaning:</b></p>
        <p>Data Cleaning techniques applied includes:	
            <br>• Tokenization: This involves splitting the text into separate parts, called tokens.
            <br>• Removal of Stop words, punctuation, and special characters: Stop words are words such as articles, prepositions etc (e.g., ‘a’, ‘the’, ‘in’) which occur frequently but which aren’t particularly useful in text mining. RegexpTokenizer was used from NLTK (Natural Language Toolkit) library to transform characters like sentences into tokens (split sentences into words). It also defines a regular expression so that only alphanumeric characters are tokenized. 
            <br>• Convert all letters in a word to lower case
            <br>• Stemming: Stemming involves reducing words into a root form– this is useful because it reduces the number of unique tokens while preserving semantics (e.g., cleaned, cleaning and clean would all be reduced to clean. Stemming was used as an alternative to lemmatisation which is more difficult to use as it requires us to correctly specify the intended part of speech (lemma)of each word. 
            </p>
       <p><b>Analytical Technques and Tools:</b></p>
This project used text mining techniques and Natural Language processing algorithm in Python library to conduct sentiment analysis. Python visualisation tool like plots, word cloud etc. were used to visualise results.
               <p><b>Task/Implementation:</b></p>
        <p> Sentiments intensity Analysis using SentimentIntensityAnalyzer within NLTK library which has a pre-trained model called VADER (Valence Aware Dictionary for Sentiment Reasoning) which can estimate both sentiment polarity (whether it is positive or negative) and intensity (how strongly positive or negative it is).Based on the objective of this study, which is to identify 30 Hotels from the study dataset and perform text mining technique and sentiment analysis on data selected, a new table was created for 30 selected hotel review records based on low frequency of reviews for these selected hotels, restaurants, and bars making it a total of 2689 records to analyse. Summary of the dataset table shows that out of 2689 reviews 1042 are unique reviews which means 60% of reviews are similar. <br> Also, the project shows that 30 hotels and restaurant are from 11 locations in Thailand.  
           <p><b>Results/Outcome:</b></p> 
        <p> Le Brooklyn Patong in Patong recorded the highest number of reviews (93) while the most frequent review is a bad review that occurred 10 times.
            Sentiment analysis was conducted on the sampled reviews and sentiment polarity of negative and positive reviews shows that most reviews were positive although, the density of positive sentiments distribution is more towards the left (right skewed) and fewer towards the extreme positive sentiment of 1. Also, the density of negative polarity score distribution is very scanty where few negative reviews are concentrated more on zero than towards the extreme negative point of 1. This was further depicted by the compound polarity score distribution, where scores lower than zero are negative sentiments and their level of intensity, and scores higher than zero are positive sentiments (Distribution was left skewed as expected).Further review of hotels, restaurants, and bars by percentage of negative reviews (reviews with compound less than or equal to zero) identifies Dada Yura Restaurant as the tourist accommodation with the highest percentage negative review hence this study will further analyse reviews of Dada Yura Restaurant to identify these negative review words for more insights. Moreso, analysis of percentage positive reviews (reviews with compound more than zero) showed that Chekhoff Restaurant and Bar had a 100% positive reviews, however this assumption was evaluated using text mining techniques to view frequency distribution of the positive reviews and corresponding word cloud.The word cloud and frequency distribution of negative reviews of Dada Yura Restaurant (refer to figure 3 and 4) depicted some insights which could better inform the restaurant management on what to improve. They are as follows:
           <br> •	Bad review about the staff in the restaurant
           <br> •	Restaurant appears Untidy and messy to some customers
           <br> •	Poor Service rendered by staff 
           <br> •	The food taste was horrible for some customers
            <br>It is also observed that some customers said nice things too about services and food especially dinner considering the word cloud of the positive reviews for the restaurant.
            </p>
        <p>In summary, the ability of text mining and sentiment analysis to provide good insights of customer opinions to businesses has been achieved in this study. Selection of hotels and restaurants based on lowest reviews as selection criteria provides great insights to why the reviews are low recommending what could be worked on to increase positive customer reviews based on generated word clouds and frequency distribution of review words in case study hotels and restaurant (Dada Yura restaurant in Patong selected based on highest percentage negative review and Chekhoff Restaurant and bar selected based on highest percentage positive review). These insights would be useful by management and decision makers of hotels, restaurants and bar in the study locations create better customer experience in tourism industry. 
            <br>Python Notebook for the full code of this project can be seen using this link <a href = "https://colab.research.google.com/drive/1URc_m3StNJQP3-0lENI89iMpdIviBHHd?authuser=1"> <b>Click here to view project codes</b></a></p>
      </div>
      <div class="project">
        <h3> ARTIFICIAL INTELLIGENCE FAIRNESS: METHODS TO DETECT AND MITIGATE BIAS</h3>
           <p><b>Project Overview:</b></p>
        <p>It is important to ensure that AI is not used to perpetuate existing biases or discrimination. This study therefore explored AI Fairness 360 (AIF360) Python library by IBM, that consists of fairness metrics and algorithms that can mitigate bias in machine learning workflow. .</p>
         <p><b>Dataset:</b></p>
          <p>Study datasets were processed datasets from the AIF360 package namely adult census dataset, German scoring dataset and COMPAS recidivism dataset. These datasets were cleaned from null values, encoded for binary classification and normalised for unifrom variable scale. These datasets were analyzed with fairness metrics to detect bias in the training dataset</p>
        <p><b>Analytical Technques and Tools:</b></p>
          <p>Exploratoray data analysis of each dataset was done using visualisation tools in Python library such as plots and seaborn. Also Machine learning algorithm like Logistics regression and AIF360 algorithms available in Python were used in this project</p>
            <p><b>Task/Implementation:</b></p>
          <p>Using AIF360 package, reweighing algorithm was implemented, and fairness and model performance were analyzed before and after implementation of the reweighing algorithm to examine its effect on improving fairness across groups. The study used Logistics regression classifier to train model for each study dataset, predict outcomes and evaluate model performance for the three study datasets, comparing the fairness metrics and balanced accuracy of the model before and after reweighing method was implemented. </p>
        <p><b>Results/Outcome:</b></p> 
          <p>The study findings indicated that models created using the study dataset were biased against the unprivileged groups and reweighing method applied was able to significantly mitigate bias to create a fairer model for both the privileged and unprivileged group. Furthermore, the fairness-accuracy trade off was discussed in this study and the study was able to show using German dataset that fairness can also be achieved without significantly reducing model accuracy. 
             <br> Ideally this model will be useful to all AI stakeholders to ensure that AI solutions developed are fair across groups, thereby upholding ethical AI.
              <br>Python Notebook containing the full code of this project can be seen with this link <a href= "https://colab.research.google.com/drive/1XZ7uXwUeN0ZeYfiEWOgr_mIeb-vXPSkL?authuser=1"> <b>Click here to view project codes</b></a></p>
      </div>
  </section>
  
  <section id="skills">
    <h2>Skills</h2>
   <p><b>Data Visualization and Reporting:</b>
<br>Power BI Dashboards, Microsoft Excel reporting and Dashboards, Tableau Dashboards.
</p>
<p><b>Data Analysis and Manipulation:</b>
<br>MySQL,PostgreSQL, Python and R.
</p>
<p><b>Machine learning Modelling and Deep Learning algorithms:</b>
<br>Supervised & Unsupervised Learning, Deep Learning and Neural Networks, CNN, Natural Language Processing (NLP), Logistics regression, XGBoost, KNN, Decision trees, Randomforest,K-Means, Clustering, Customer segmentation, Sentiment analysis .
</p>
<p><b>ML tools/frameworks:</b>
<br>Tensorflow, Keras, SciKit Learn, Numpy, Pandas, SciPy.
</p>
<p><b>Cloud Computing:</b>
<br>Tensorflow, Keras, SciKit Learn, Numpy, Pandas, SciPy.
</p>
<p><b>Big Data Technologies:</b>
<br>Big data technologies (Hadoop, Spark, and Hive), ETL (Extract,Transform, Load) development, Databricks.
</p>
<p><b>Statistical Analysis:</b>
<br>Summary statistics, Hypothesis testing, Linear regression.
</p>
<p><b>Analytical skills:</b>
<br>Research, forecasting, critical thinking, reporting, problem solving, passion for providing data-based insight.
</p>
<p><b>Soft Skills:</b>
<br>Excellent attention to details, high level written and verbal communication skills, upskilling, strong analytical skills, teamwork, presentation skill, risk management, financial analysis, application management, stakeholder management, project management, good time management, problem solving, strategizing and customer service.
</p>
  </section>
  
  <section id="contact">
    <h2>Contact Me</h2>
    <p>Feel free to reach out to me for any inquiries or collaborations.</p>
    
            <a href= "https://www.linkedin.com/in/chisom-oranebo-obazee/">
                        <img src="linkedin.png" alt="linkedin logo"class="social">
            </a>

            <a href= "https://github.com/chisomoranebo">
                        <img src="GitHub-logo.png" alt="GitHub logo" class="socials">
            </a>
            
  </section>
  
  <footer>
    <p>&copy; 2023 My Data Science Portfolio. All rights reserved.</p>
  </footer>
</body>
</html>
