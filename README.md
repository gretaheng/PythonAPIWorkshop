# Using APIs to Collect Data from Media/Social Media Sources
This workshop assumes attendees are familiar with the basics of Python and Jupyter Notebook but all are encouraged to attend. We will learn about APIs (Application Program Interface) and use the New York Times Article Search API as an example to collect data returned from the API with Python. Then we will parse the messy data output into something meaningful. The slides and Jupyter Notebook used in this workshop can be found here.

## Request a New York Time Article Search API Key
- Go to the New York Times (NYT) Developer website and create your account
- Look for the verification email in your inbox (spam folder) and click the link in that email
- Sign into your NYT Developer account
- Select Apps from the user drop-down
- Click + New App to create a new app
- Enter a name and description for the app in the New App dialog, enable Article Search API
- Click Create
- Select Apps from th user drop-down.
- Click the app in the list.
- View the API key on the App Details tab.
- Confirm that the status of the API key is active and copy the API key to a .txt file.

## Jupyter Notebook
Jupyter Notebooks are a powerful way to write and run your Python code. We can write lines of code and run them one at a time. To launch a Jupyter notebook, open your terminal and navigate to the directory where you would like to save your notebook. Then type the command jupyter notebook and the program will instantiate a local server at localhost:8888 (or another specified port). A browser window should immediately pop up with the Jupyter Notebook interface, otherwise, you can use the address it gives you. To run a cell, you could hit enter and shift together or click the run button on the top.

## What is an API
API is the acronym for Application Programming Interface, which is a software intermediary that allows two applications to talk to each other. By establishing a common set of rules for exchanging information, APIs make it easier for two parties to communicate with each other. Each time you use an app like Twitter, post a tweet, or check the New York Times online articles on your phone, you’re using an API. When you use an application on your phone, the application connects to the Internet and sends data to a server. The server then retrieves that data, interprets it, performs the necessary actions and sends it back to your phone. The application then interprets that data and presents you with the information you wanted in a readable way. This is what an API is - all of this happens via API. 

We could think APIs as methods of accessing data or functionality from business or government organization. We can use a simple API call to retrieve data instead of having to code it by ourselves. Suppose you want to collect all tweets posted by Barack Obama. Of course, you can do that manually on twitter. But it can take a long time. Using Twitter API largely improves the efficiency of data collection because you only need to run a few lines of code and data can be collected automatically.

## Media and Social Media APIs
Some media and social media companies make their data banks on users and usage patterns available through their APIs, such as New York Times, Bloomberg, Youtube, Instagram, Facebook, and Twitter. We can access the API to retrieve, store, and manipulate about users for analysis. Please note that while APIs make data publicly available, they are not open in the sense of giving full and unlimited access to the entire database of companies such as Twitter and Facebook because of privacy and legal concerns.

There are many kinds of studies we could do using the data we get from media and social media companies. We can build the semantic network in articles, find topics of a corpus, or visualize the relationships of your twitter followers. 

## REST APIs
Rest stands for representational state transfer. It relies on the HTTP protocol and JSON data format to send and receive messages. What does it mean? Let’s say you’re trying to find articles about COVID on the New York TImes. You open up The New York Times official website, type “COVID” into a search field, hit enter, and you see a list of articles about this virus. You may notice the url showing on the top of the browser reflect your request (https://www.nytimes.com/search?query=covid). A REST API works in a similar way. You search something, generate a special url representing you request, and get a response back from the service you’re requesting from. But instead of a HTML webpage, you get the data in JSON format. The url request uses a suitable HTTP method and includes a query and an api key (url = https://api.nytimes.com/svc/search/v2/articlesearch.json?q=COVID&api-key=[YOUR_API_KEY]).

### Request
*HTTP Methods*: When you search information about NYT or Twitter APIs, you may find the word GET somewhere on the webpage. Get is a http method that REST APIs use to read and retrieve data. Users can also modify and create data via different HTTP methods, but our focus today is Get method.

*Parameters*: Just like the website, we could specify and narrow the scope of our API requests by providing the date range, sections, and types of article. Some APIs also allow us to sort the results by date or by relevance. To do that, we could add several query parameters in the API request. In the New York Times Article Search API, the query parameters are the optional key-value pairs that appear after the question mark in the URL. For example, this url (https://api.nytimes.com/svc/search/v2/articlesearch.json?begin_date=20200101&end_date=20200331&q=COVID&api-key=[YOUR_API_KEY]) shows that we want articles about COVID that were published between January 2020 and March 2020. Different APIs may have different parameters. Please read the API documentation carefully when you construct your URL request.

*API key & Access Token*: API key is a value that identifies your application and your requests. If an API requires a key, you must first be accepted as a user of the service to get your personal identifier, the API key. When you call the API, the API key is part of the request you make to the services. With the API key, the services can identify you, log which service you are using, accept your requests if the API key is valid, and send you the appropriate data. Therefore, an API key is for identification and authorization. For some APIs, like twitter API, apart from API key, you will also need access token because token is part of authentication. Access Token is user-specific, I can generate a token for myself. I can also generate one for my friend. But when I log into my project, I have to use the token that is associated with my account not my friend’s.

### Response
For our concerns today, we submit a request to the server endpoint via a URL and the response is returned as JSON data. JSON is an acronym for JavaScript Object Notation, which is. It is easy for humans to read and write, and easy for machines to parse and create. JSON is a text format that is built on name-value pairs. In python this is referred to as a dictionary. The value can be a string, a dictionary or a list. We parse this data just like we process any python dictionary.

## Self-learning resources
- Request for Twitter API: https://rapidapi.com/blog/how-to-use-the-twitter-api/
- Tweepy Python Library: https://docs.tweepy.org/en/v3.5.0/getting_started.html
- Mining twitter data with Python: https://marcobonzanini.com/2015/03/02/mining-twitter-data-with-python-part-1/comment-page-1/

## Reference
[What is an API?](https://www.mulesoft.com/resources/api/what-is-an-api)
