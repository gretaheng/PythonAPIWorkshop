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

## What is API
API is the acronym for Application Programming Interface, which is a software intermediary that allows two applications to talk to each other. By establishing a common set of rules for exchanging information, APIs make it easier for two parties to communicate with each other. Each time you use an app like Twitter, post a tweet, or check the New York Times online articles on your phone, you’re using an API. When you use an application on your phone, the application connects to the Internet and sends data to a server. The server then retrieves that data, interprets it, performs the necessary actions and sends it back to your phone. The application then interprets that data and presents you with the information you wanted in a readable way. This is what an API is - all of this happens via API. 

We could think APIs as methods of accessing data or functionality from business or government organization. We can use a simple API call to retrieve data instead of having to code it by ourselves. Suppose you want to collect all tweets posted by Barack Obama. Of course, you can do that manually on twitter. But it can take a long time. Using Twitter API largely improves the efficiency of data collection because you only need to run a few lines of code and data can be collected automatically.

