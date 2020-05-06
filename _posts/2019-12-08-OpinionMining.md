---
title: "Opinion Mining of Cellphone Reeviews"
date: 2019-12-08
tags: [Python, Cellphone Reviews, Programming, Data Science, Data Visualization, Data Analysis, Machine Learning, NLP]
header:
  image: "/images/NathanPhillips.jpg"
categories: DataScience
---
Analysis of the opinions people have on features available in cellphones through Amazon rewiews.

Data Summary: Date, Content, Rating, Review Month.

Description: In this project, the product reviews of two Smartphones namely the Samsung Galaxy S10 and the iPhone XR are scrapped from the amazon e-commerce website. Further, data cleansing is performed and only the necessary attributes are selected from the scrapped data. Each review is broken down into sentences. Certain explorative data analysis is performed on the data and graphs are plotted.

Reviews can be broadly categorized into two types - Objective reviews and subjective reviews. Objective reviews are the ones where facts about the device are stated and this information can be easily verified. For example, ‘the iPhone X has a 12- megapixel primary camera’. Subjective reviews are the reviews that are subjective to the experience a user had with the device. For example, ‘the pictures shot on the iPhone X are stunning’. Here, the word ‘stunning’ is used to describe the pictures taken on an iPhone X. In our case, we are interested in the subjective reviews. We use certain classification models such as SVM, Random Forest and Naieve Base Algorithm to perform the classification. Also, the performance of these models is compared to select the optimum model. Further, lexical based approach is utilized to provide a percentage positive and percentage negative rating to the features of both the devices. This summarization can help the customer make better decisions.

Please refer the file Final_Report_Suraj_Suresh_Sajjan for the detailed project report here: [**OpinionMining**](https://github.com/SurajSajjan/ANCOVA/blob/master/ANCOVA_Report.pdfhttps://github.com/SurajSajjan/OpinionMiningCellphoneReviews/blob/master/Final_Report_Suraj_Suresh_Sajjan.pdf){:target="_blank" rel="noopener" }