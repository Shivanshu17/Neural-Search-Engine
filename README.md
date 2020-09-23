# Neural-Search-Engine

## Problem Overview
Natural Language search, Formalized (structured) Query Creation, and Retrieval of most Relevant results (ranked according to pertinence), these three tasks constitute almost all of the search engine’s fundamental tasks. Each of these subtasks have a tremendous role to play in the efficacy of a search engine.
 In this project, I’ll try to approach a segment of the first task, Natural Language Search - Autocomplete Feature. This feature provides suggestions to the users in real time as they are typing in the query. The suggestions should mirror the user’s intent, while ensuring that there’s a reasonable index in the search engine to match the query. This task can be coupled with the task of producing a Document Ranking metric based on vector space representations of documents and the search queries.

## Client Case Study
Imagine a large E-Commerce giant - Amazon or Flipkart! Now, consider the amount of queries they must have to handle in their search box. And just like Google queries, almost every potential customer would expect the search bar to assist in the searching process, and produce meaningful recommendations, even if the query isn’t well structured.
Facilitating a powerful search engine just for the sake of improved User Experience (which then translates into more business) is a reason enough for industries to invest resources in this direction. Couple this with the fact that users nowadays are prone to writing descriptive queries for the (specific) items they are want, [for eg. - “White netted sneakers with blue stripes and low ankle height and canvas finish”] you have got yourself something essential that the company’s search engine got to have (if they want to retain the customer). 
This isn’t just limited to E-Commerce companies. Any organization with a high amount of B2C interactions with a wide array of items that the user’s could engage with, would benefit from incorporating an advanced and sophisticated architecture of their search engine. This effort can lay fruit in integrating their item search queries with Google’s search queries to ensure a higher number of clicks. 
The dataset being used for this project provides us with the room to engage in development of simple (yet fundamental) components of search engines. The autosuggest mechanism for search queries has been shown in multiple studies to improve the number of clicks on the page, and the fact that we could even rank the documents (once the queries have been made), adds to the relevance of this project.

## Data Used
Based on the tasks that I have identified for this project, the ideal data set will have the following two characteristic components:
Would have tons of queries from the users.
Would (preferably) also contain the indexed textual elements of the documents being searched for. Like title, summary, author, salient points, etc.
Fortunately this two requirements are satisfied in the dataset:
 TREC-2019-Deep-Learning - https://microsoft.github.io/TREC-2019-Deep-Learning/
The main goal for producing this dataset was to study the methods that work best in the domain of Information Retrieval. With following fundamental questions laying the founding stones for creation of the dataset - Do the same methods that work on small data also work on large data? How much do methods improve when given more training data? What external data and weak supervision can be brought in to bear in this scenario, and how useful is to combine full supervision with other forms of supervision including transfer learning?
With these fundamental questions in mind, TREC has provided data from msn searches query log. They have included the search queries, document corpus, and 100 rankings of the documents pertaining to each query (baseline). I have described specifics of the dataset underneath.
The dataset is divided into three fundamental components that are listed below:
#### Queries Data:
No. of Data Instances - 1,010,916
**Data Fields:**
qid -> Unique Id for the query
query -> Text of the query itself.
#### Corpus Data
No of Data Instances - 8,841,823
**Data Fields:**
pid ->Unique document id
passage -> Content of the passage
#### Ranking Data
No. of Data Instances - 36,701,300 (I’d pull it down to 200,000 by random sampling)
**Data Fields:**
qid -> Id of the Query
pid -> Id of the document
query -> Query on the search engine
passage -> The corresponding passage that is best suited

