# SLO Document

This exercise aims to learn how to define SLOs for a user journey.

## Exercise Rules

- Create an exercise documentation (en|de) while you are working on the tasks.
- For every task, write down your initial thoughts, assumptions, and the final outcome in full sentences. Describe the process of solving the task.
- If you are not able to solve the task, describe how you would solve it theoretically. You should still provide a step by step description from the documentation or tutorial you found.
- Provide a reference for every documentation or tutorial you used to solve a task. Paraphrase and cite correctly, please.
- Your submission should be described in __at least two, but not more than three A4 pages__.

## Tasks

1. Read the description of the web app 'The Shop' - a webshop for gaming pc hardware. Also, read the description of 'Persona X'. This person is a typical user of 'The Shop'. Describe the user's steps to finally purchase an item in full sentences - this is the user journey.
2. You will create an SLO document for this user journey. Take a look at this example before you go on: [Example SLO Document](https://sre.google/workbook/slo-document/)
3. Find 3-5 SLIs for this user journey and explain why each of the SLIs is essential for what aspect of the user journey. None of the SLIs is allowed to measure the same aspect. An example for an aspect is the search speed, defined by the time elapsed between sending a search request and the full rendering of visible search results.
4. What SLI category does each SLI have?
5. Where is each SLI measured? Possible metric sources could be:
      - a distinct service
      - the load balancer
      - customer-support tickets
      - customer survey
      - post-mortem documentations
      - management reports
      - review or recommendation platforms
      - or others
6. How is each SLI measured? Possible measuring methods could be:
      - aggregation of metrics
      - collection of logs
      - regular probing (monitors)
      - scraping of web site content
      - usage of external APIs
      - or others

7. 100% Reliability is not the goal, also ultra-high performance is not - because of the high costs it will produce. Define SLOs for each SLI and reason about the importance of ambitious 'good' values for each of them - when is 'average' good enough? Example: Is a fast search more important than a fast checkout? When and why does this statement apply regarding our user journey?

### Application: 'The Shop'

'The Shop' is a webshop for a wide range of gaming pc hardware components. This store is popular with hobbyists who want to assemble their pc on their own. There are regular sales, and the pricing of individual items can change within days.
Architecture-wise, four main backend services are running:

#### Search

This service is optimized for delivering fast results when users perform a search for products. It does not manage all of the actual product data but provides key data such as title, price, category, rating, and the URL of the main product image. Every search result delivers a list of products with this metadata so that the frontend can show each product's key data in the result list.

#### Product

This service delivers the whole data for a product, such as more images and technical specifications. The product service comes into play when a user clicks on a search result to display the product's detail page.

#### Cart

This service is rather small; it listens for events that put products into the cart and manages the user session. The cart service provides a list of products for the checkout.

#### Checkout

This service gets the cart information and handles the payment process, including shipping addresses and order confirmation.

### User: Persona X

Persona X is on a budget. This person has several concrete pc hardware components on their wish list and hopes for good prices. At least weekly, this person looks for better prices in 'The Shop' for items on their wish list (Bookmarks). The purchasing process is already running for several weeks, only to get the best price.

## This will help you!

- Using a search engine
- [The Art of SLOs - Handbook](https://static.googleusercontent.com/media/sre.google/en//static/pdf/art-of-slos-handbook-a4.pdf)
- [Example SLO Document](https://sre.google/workbook/slo-document/)

> ![Exercise](https://user-images.githubusercontent.com/7222193/149557234-27d1309c-4a52-4d3b-a0b7-77222bfc6f36.png)

