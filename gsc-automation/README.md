
# GSC_Get_Clicks_Impressions_Multi_Links

### Google Search Console API Authentication

Getting your key is easy! Just follow these simple steps:
- Sign in to your [Google API Console](https://console.developers.google.com/).
- Go to "**Dashboard**" and click "**Enable APIs and Services.**"
- Find "**Google Search Console API**" and enable that.
- Go to "**Credentials**", click "**Create Credentials**" and choose "**OAuth Client ID.**"
- Name your product when asked to "**Configure the Consent Screen.**"
- Select "Other" as the application type and click "**Create.**"
- Copy your client ID and client secret. You can also download them as a JSON file.

For detail, follow this [Google Search Console API documentation](https://developers.google.com/webmaster-tools).

### Download Repo and Run Scripts in Google Colab

To this this repository:
- Follow the official GitHub documentation: This guide provides detailed instructions on downloading files from [GitHub](https://docs.github.com/en/get-started/start-your-journey/downloading-files-from-github).

To upload downloaded python scripts to Google Colab
- Once you have downloaded the repository, you'll need to upload the scripts to Google Colab to run. Here's [a helpful resource to get started with Google Colab](https://www.geeksforgeeks.org/how-to-use-google-colab/).

### Configure authentication, time range & Replace URLs in Script

Update your client_id & client_secret:
```
# Use Your Google Cloud Project Client ID & Client Secrets
CLIENT_ID = "<your-client-id>"
CLIENT_SECRET = "<your-client-secret>"
```

Replace your main site URL, URLs that you want to get clicks and impressions count and Date Range.
```
site_url = 'https://www.example.com/'

# URLs provided as a multi-line string
url_list = """
https://www.example.com/home
https://www.example.com/pages/1
https://www.example.com/pages/2
"""

# Start and end dates for the data
start_date = '<YYYY-MM-DD>'
end_date = '<YYYY-MM-DD>'
```
### Downloading the Output CSV File

Once the script finishes running, it will generate a CSV file named "**search_console_data.csv**" within the Colab runtime folder. This file contains data on clicks and impressions for your multiple URLs.

To download the CSV File:
- In the Colab interface, navigate to the **left sidebar** and locate the "**Files**" tab. You can see the "search_console_data.csv" file listed. Right-click on the file and select "Download."