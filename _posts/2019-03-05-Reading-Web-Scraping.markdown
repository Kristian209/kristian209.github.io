---
layout: post
title:  "Data lit: Reading Assignment(1.5)Web Scraping Techniques"
date:   2019-02-28 12:49:44 -0800
categories:  data lit
---
*What is Web Scraping?*

Web Scraping is a technique used to extract data from websites through an automated
process.

*Use Cases*

- One could compare the prices of two different websites by scraping their pages
- One could be alarmed if a price of a flight ticket is lowered by crawling the
travel websites

*Golden Rule*

**BE NICE TO THE SERVERS; YOU DON'T WANT TO CRASH THE WEBSITE**

**Steps Using BeautifulSoup w/ Requests**
1. You need to understand the website's structure.
   - Inspect the HTML website using your browsers "inspect" option
2. Import the libraries, do the request, parse the html and then find the class
main_price
3. Avoid pitfalls
   - Check robots.txt
   - Use specific id rather than class since it is less likely to be changed
   - Check if the element returns None
   - User agent spoofing because every time you visit a website, it gets your
   browser info via "user agent"
   - Timeout requests because by default Request will keep waiting for a response
   indefinitely
   - Frequent code appearances like 404(Not Found), 403(Forbidden), 408(Request Timeout)
   might indicate you got blocked
   - Make sure to rotate your ip by using shared proxies, VPNs or TOR which help you
   become a ghost
   - Be careful with Honeypots which are means to detect crawlers and scrapers
4. Dos & Don'ts
   - Check for public APIs before scraping, they are easier and faster at data retrieval
   - Consider using a database to analyze and retrieve large amounts of data fast
   - Be polite. Let people know you are scraping their site
   - DO NOT OVERLOAD THE WEBSITE  
5. Speed up - Parallelization
   - If you extract a huge amount of info from the page and do some preprocessing
   of the data while scraping, the number of requests per second you send to the page
   can be relatively low.
