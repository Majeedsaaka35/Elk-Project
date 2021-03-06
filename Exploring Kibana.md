## Activity File: Exploring Kibana

* You are a DevOps professional and have set up monitoring for one of your web servers. You are collecting all sorts of web log data and it is your job to review the data regularly to make sure everything is running smoothly. 

* Today, you notice something strange in the logs and you want to take a closer look.

* Your task: Explore the web server logs to see if there's anything unusual. Specifically, you will:

:warning: **Heads Up**: These sample logs are specific to the time you view them. As such, your answers will be different from the answers provided in the solution file. 

---

### Instructions

1. Add the sample web log data to Kibana.

2. Answer the following questions:

    - In the last 7 days, how many unique visitors were located in India?
      - 250

    - In the last 24 hours, of the visitors from China, how many were using Mac OSX?
      - 11

    - In the last 2 days, what percentage of visitors received 404 errors? How about 503 errors?
      - 404: 5.556%
      - 503: 5.556%
    
    - In the last 7 days, what country produced the majority of the traffic on the website?
      - China
    
    - Of the traffic that's coming from that country, what time of day had the highest amount of activity?
      - 12pm
    
    - List all the types of downloaded files that have been identified for the last 7 days, along with a short description of each file type (use Google if you aren't sure about a particular file type).
      - Gz - an archive file that has a compressed collection of multiple files.
      - Css- this shows how HTML elements are displayed on a screen.
      - Zip- this compresses files to reduce the file size.
      - Deb-  this is a debian package that has gzipped archives and is mostly used for Unix-based operating systems.
      - Rpm- a red hat package manager is used to store installation packages on Linux operating systems.


3. Now that you have a feel for the data, Let's dive a bit deeper. Look at the chart that shows Unique Visitors Vs. Average Bytes.
     - Locate the time frame in the last 7 days with the most amount of bytes (activity).
     - In your own words, is there anything that seems potentially strange about this activity?
       - This activity only shows 1 count for over 15 thousand bytes.

4. Filter the data by this event.
     - What is the timestamp for this event?
       - 7/25/2021 at 21:00
     
     - What kind of file was downloaded?
       - RPM File
     - From what country did this activity originate?
       - India
     - What HTTP response codes were encountered by this visitor?
       - 200 (OK)

5. Switch to the Kibana Discover page to see more details about this activity.
     - What is the source IP address of this activity?
       - 28.11.251.5

     - What are the geo coordinates of this activity?
       - { "lat": 43.16552778, "lon": -95.20280556 }
     
     - What OS was the source machine running?
       - OSX
     - What is the full URL that was accessed?
       - https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-6.3.2.zip
     
     - From what website did the visitor's traffic originate?
       - http://twitter.com/success/aleksandr-misurkin

6. Finish your investigation with a short overview of your insights. 

     - What do you think the user was doing?
       - Downloading a zip file
     - Was the file they downloaded malicious? If not, what is the file used for?
       - No. Zip files are used to compress one or more files.
     
     - Is there anything that seems suspicious about this activity?
       - No
     
     - Is any of the traffic you inspected potentially outside of compliance guidlines?
       - No
