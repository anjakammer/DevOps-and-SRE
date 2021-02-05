# Scenario: 'The Shop'

## Application Architecture

'The Shop' is a webshop for a wide range of gaming pc hardware components. This store is popular with hobbyists who want to assemble their pc on their own. There are regular sales, and the pricing of individual items can change within days.
Architecture-wise, four main backend services are running:

### Search

This service is optimized for delivering fast results when users perform a search for products. It does not manage all of the actual product data but provides key data such as title, price, category, rating, and the URL of the main product image. Every search result delivers a list of products with this metadata so that the frontend can show each product's key data in the result list.

### Product

This service delivers the whole data for a product, such as more images and technical specifications. The product service comes into play when a user clicks on a search result to display the product's detail page.

### Cart

This service is rather small; it listens for events that put products into the cart and manages the user session. The cart service provides a list of products for the checkout.

### Checkout

This service gets the cart information and handles the payment process, including shipping addresses and order confirmation.

### other Components

The application has clearly also other components, that you can come up with yourself.

## User: Persona X

Persona X is on a budget. This person has several concrete pc hardware components on their wish list and hopes for good prices. At least weekly, this person searches in 'The Shop' for better prices for items on their wish list. The purchasing process is already running for several weeks, only to get the best price.

## Special Event: Black Friday

Black Friday is the most intense event of the year for 'the Shop'. There are special measures taken, to increase the scalability of the architecture, at moderate costs for the rest of the year.
