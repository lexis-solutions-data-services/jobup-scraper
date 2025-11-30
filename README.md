# Jobup.ch Jobs Scraper

![banner](https://lexis-solutions-apify.fra1.cdn.digitaloceanspaces.com/banners/jobup-ch.png)

👋 Welcome to the Jobup.ch Scraper, an actor designed to help you gather job listings from Jobup.ch! With this actor, you can easily search for job listings based on job query and location in Switzerland.

<p align="center">
  <img src="https://apify-image-uploads-prod.s3.us-east-1.amazonaws.com/DevbkY3adMTBuoECt-actor-M3DOBpkaS6Jtde2Xu-Dkb4W0UrGb-unnamed_%289%29.png" alt="Jobup Scraper" style="height: 60px; margin-right: 15px;" /><a href="https://apify.com/lexis-solutions/jobup-scraper" target="_blank">
    <img src="https://img.shields.io/badge/Try%20it%20on-Apify-0066FF?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDA4IiBoZWlnaHQ9IjQwOCIgdmlld0JveD0iMCAwIDQwOCA0MDgiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxnIGNsaXAtcGF0aD0idXJsKCNjbGlwMF8zNDFfNDE1NykiPgo8cGF0aCBkPSJNMjE4LjY5NSAxMDRIMzAwLjk3QzMwMi42NDMgMTA0IDMwNCAxMDUuMzU3IDMwNCAxMDcuMDNWMjMyLjc2NkMzMDQgMjM1Ljc3OCAzMDAuMDgzIDIzNi45NDUgMjk4LjQzNCAyMzQuNDI1TDIxNi4xNTkgMTA4LjY5QzIxNC44NDEgMTA2LjY3NCAyMTYuMjg3IDEwNCAyMTguNjk1IDEwNFoiIGZpbGw9IndoaXRlIi8+CjxwYXRoIGQ9Ik0xODkuMzA1IDEwNEgxMDcuMDNDMTA1LjM1NyAxMDQgMTA0IDEwNS4zNTcgMTA0IDEwNy4wM1YyMzIuNzY2QzEwNCAyMzUuNzc4IDEwNy45MTcgMjM2Ljk0NSAxMDkuNTY2IDIzNC40MjVMMTkxLjg0IDEwOC42OUMxOTMuMTU5IDEwNi42NzQgMTkxLjcxMyAxMDQgMTg5LjMwNSAxMDRaIiBmaWxsPSJ3aGl0ZSIvPgo8cGF0aCBkPSJNMjAyLjU5MSAyMDQuNjY4TDEwOS4xMjcgMjk4LjgzNUMxMDcuMjI5IDMwMC43NDcgMTA4LjU4MyAzMDQgMTExLjI3OCAzMDRIMjk2LjhDMjk5LjQ4MyAzMDQgMzAwLjg0MiAzMDAuNzcgMjk4Ljk2NyAyOTguODUyTDIwNi45MDggMjA0LjY4NUMyMDUuNzI2IDIwMy40NzUgMjAzLjc4MiAyMDMuNDY4IDIwMi41OTEgMjA0LjY2OFoiIGZpbGw9IndoaXRlIi8+CjwvZz4KPGRlZnM+CjxjbGlwUGF0aCBpZD0iY2xpcDBfMzQxXzQxNTciPgo8cmVjdCB3aWR0aD0iMjAwIiBoZWlnaHQ9IjIwMCIgZmlsbD0id2hpdGUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEwNCAxMDQpIi8+CjwvY2xpcFBhdGg+CjwvZGVmcz4KPC9zdmc+Cg==&logoColor=white" alt="Try it on Apify" style="border-radius: 12px; height: 60px;" />
  </a>
</p>


## Introduction

## 📊 Actor Stats

| Stat | Value |
|------|-------|
| **Version** | `0.0.6` |
| **Last Update** | Nov 30, 2025 |

---



The Jobup.ch Scraper is a web scraping tool designed to extract job listings from Jobup.ch. It was created to make it easier for job seekers and recruiters to find relevant job postings in the Swiss job market and make data-driven decisions based on the extracted information.

## Use Cases

Here are some typical scenarios in which the Jobup.ch Scraper can be useful:

- **Job seekers** can use the scraper to find job listings that match their skills and experience in Switzerland.
- **Recruiters** can use the scraper to monitor the Swiss job market and stay up-to-date on the latest job openings.
- **Researchers** can use the scraper to gather data on job trends and analyze the Swiss job market.

## Input 📥

To use this actor, you need to provide the following input:

- Field: **startUrls**
  - Type: array
  - Required: No
  - Description: URLs to start with.
  - Example: `[{"url": "https://www.jobup.ch/en/jobs/?location=berne&term=sales"}]`
- Field: **search**
  - Type: string
  - Required: No
  - Description: Enter search
- Field: **location**
  - Type: string
  - Required: No
  - Description: Enter location
- Field: **maxItems**
  - Type: integer
  - Required: Yes
  - Description: Limit the number of items to be scraped (0 for unlimited)
  - Default: 10
- Field: **proxyConfiguration**
  - Type: object
  - Required: No
  - Description: Your proxy configuration from Apify
  - Default: `{"useApifyProxy": true, "apifyProxyGroups": []}`

Note: You must provide either `search` and `location` parameters or `startUrls`. The `maxItems` parameter is required.

## Output 📤

An example output looks like this:

```json
{
  "url": "https://www.jobup.ch/en/jobs/detail/df39643f-6296-4a0a-88f0-18386d2f983a/",
  "title": "Boutique Manager",
  "companyName": "Compagnie des Montres Longines Francillon SA",
  "publicationDate": "2025-03-10T12:10:22+01:00",
  "place": "Saint-Imier",
  "street": "",
  "employmentGrades": "100",
  "email": "daphne.lechenne@longines.com",
  "zipCode": "2610",
  "description": "<!DOCTYPE html>...</html>",
  "descriptionPosition": "Boutique Manager",
  "descriptionText": "Introduction de la société...",
  "isActive": true,
  "lon": 6.997923,
  "lat": 47.152083,
  "isPaid": true,
  "contactPerson": "",
  "location": ""
}
```

## How many job listings can the Jobup.ch Scraper extract?

The Jobup.ch Scraper uses pagination to extract all job listings from Jobup.ch. You can control the number of job listings to scrape by setting the `maxItems` input parameter. If you don't set the `maxItems` parameter, the scraper will extract all job listings available on the website.

## Why use the Jobup.ch Scraper?

- ⚡️ **Fast** - The scraper is fast and efficient, allowing you to scrape job posts in a programmatic way.

- 🤙 **Easy to use** - The scraper is easy to use and requires no coding knowledge. All you need to do is input the query you want to scrape and the scraper will do the rest.

- ☑️ **Well-Maintained** - The scraper is maintained by the Lexis Solutions team, ensuring that it is always up-to-date and working properly.

## FAQ 💬

- **What is Jobup.ch?**

  Jobup.ch is one of Switzerland's leading job sites that allows job seekers to search for job listings and apply for positions online. It also provides tools for employers to post job openings and manage applications.

- **How can I find jobs on Jobup.ch?**

  You can find jobs on Jobup.ch by visiting the website and using the search function to look for job listings that match your criteria. The Jobup.ch scraper automates this process by extracting job listings based on the criteria you specify in the input.

- **Can I use the Jobup.ch scraper to apply for jobs?**

  No, the Jobup.ch scraper is intended for data extraction and analysis purposes only. It should not be used to apply for jobs or otherwise interact with Jobup.ch's website.

- **What types of jobs can the Jobup.ch scraper find?**

  The Jobup.ch scraper can find any job posted on Jobup.ch that matches the criteria you specify in the input. The platform primarily focuses on jobs in Switzerland.

- **What if the website changes?**

  It is possible that changes to the website's structure or code may break the scraper. In this case, the scraper will need to be updated to reflect the changes in order to continue working properly. It is important to regularly monitor the website for any changes that may impact the scraper's functionality and update it as needed.

## Need to scrape other job boards in Europe?

- UK 🇬🇧

  - [Reed.co.uk Scraper](https://apify.com/lexis-solutions/reed-co-uk-scraper)
  - [TotalJobs Scraper](https://apify.com/lexis-solutions/totaljobs-scraper)

- Germany 🇩🇪

  - [Arbeitsagentur Scraper](https://apify.com/lexis-solutions/bundesagentur-fur-arbeit-arbeitsagentur-scraper)

- Netherlands 🇳🇱

  - [Werk.nl Scraper](https://apify.com/lexis-solutions/werk-nl-scraper)

- France 🇫🇷
  - [HelloWork Scraper](https://apify.com/lexis-solutions/hellowork-scraper)

---

👀 p.s.

Got feedback or need an extension?

Lexis Solutions is a [certified Apify Partner](https://apify.com/partners/find). We can help you with custom solutions or data extraction projects.

Contact us over [Email](mailto:scraping@lexis.solutions) or [LinkedIn](https://www.linkedin.com/company/lexis-solutions)

## Support Our Work 💝

If you're happy with our work and scrapers, you're welcome to leave us a company review [here](https://apify.com/partners/find/lexis-solutions/review) and leave a review for the scrapers you're subscribed to. It will take you less than a minute but it will mean a lot to us!

Image Credit: https://www.jobup.ch
