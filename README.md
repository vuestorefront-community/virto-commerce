<div align="center">
  <img src="https://user-images.githubusercontent.com/1626923/137092657-fb398d20-b592-4661-a1f9-4135db0b61d5.png" alt="Vue Storefront" height="80px" />
</div>


---------

# #TechForUkraine

<table>
  <tr>
    <td style="width:40%;">
       <img src="https://user-images.githubusercontent.com/1626923/155853691-d6d0a541-d3b9-40bf-b8f5-2d38303e9e49.png" />
    </td>
    <td>
      <h2><strong>Ongoing tensions on Ukrainian territory close the space for civil society.</strong></h2>
      <h3>How can you support Ukrainian civil society?</h3>
      All the help is valid, and if you are not able to help locally, by giving shelter to a fellow Ukraine, there are some ways that you can help also:
      <ul>
        <li>
          Support the Ukraine Armed forces directly by sending funding to the open special accounts.<br />
          <a href="https://bank.gov.ua/en/news/all/natsionalniy-bank-vidkriv-spetsrahunok-dlya-zboru-koshtiv-na-potrebi-armiyi" target="_blank">NBU Opens Special Account to Raise Funds for Ukraine’s Armed Forces</a>
        </li>
        <li>
          Help the ICRC (Red Cross) with donations.<br />
          <a href="https://www.icrc.org/en/where-we-work/europe-central-asia/ukraine" target="_blank">Ukrainian Red Cross Society</a>
        </li>
        <li>
          Donate to the United Help Ukraine.<br />
          <a href="https://unitedhelpukraine.org/" target="_blank">United Help Ukraine</a>
        </li>
        <li>
          Donate to Voices of Children<br />
          <a href="https://voices.org.ua/en/" target="_blank">Voices of Children</a>
        </li>
    </td>
  </tr>
</table>

---------

# Vue Storefront Next VirtoCommerce Integration

> **Disclaimer:** This project is still in beta phase.


* [Documentation]() (WIP)
* [Demo]() (WIP)


This repository is a monorepo containing three projects:

* **api-client** - communicates with a backend;
* **composables** - exposes composable functions used to retrieve data using `api-client` and to map them to universal data formats using `getters`;
* **theme** - `nuxt` project that glues everything together. It extends our core theme and uses `composables` to retrieve data.


The integration is already configured to work with VirtoCommerce live demo site https://demo.virtocommerce.com.

![image](https://user-images.githubusercontent.com/7566324/106896935-eb45a800-66fa-11eb-9c8c-e6af159ea7cb.png)

# Supported features

### Category Page

- [x] I want to see a category tree so I can understand the structure of eCommerce's offer.
- [ ] I want to use filters in category page so I can limit the products visible in the category page.
- [ ] I want to use sorting in the category page so I can change the order of the products to find these easily.
- [x] I want to open the specific category so I can see products inside.
- [x] I want to use pagination in the category page so I don't have to load all the products within the category at once.
- [x] I want to see the prices on the category page so I know how much do I need to pay for the product.
- [x] I want to see the discounts on the category page so I can be attracted by lower prices.

### Navigation

- [x] I want to see the category tree so I can go through the page structure.
- [ ] I want to see breadcrumbs so I can see where I am.

### Product Page

- [x] I want to open a product page so I can see the details of the product.
- [x] I want to add a product to the cart so I can buy that in the next step.
- [x] I want to edit the quantity of the product before adding it to the cart.
- [ ] I want to change the variants of the product so I can easily switch between versions of the same master product.
- [x] I want to see the product gallery so I can see how the product looks like.
- [x] I want to see the prices on the product page so I know how much do I need to pay for the product.
- [x] I want to see the discounts on the product page so I can be attracted by lower prices.
- [ ] I want to have properties pre-selected (like colour, size) when opening the Variant Product Page.
- [ ] I want to see cross-sellings / related under the product.

### Cart

- [x] I want to open the cart so I can see the current state of my shopping basket.
- [x] I can see the totals in the cart so I know the values before I decide on placing an order.
- [x] I want to remove the product from the cart As I do not want to buy it any longer.
- [x] I want to edit the quantity of the product in a Cart Page.

### Checkout (WIP)
- [ ] I want to proceed to the checkout So I can place the order
- [ ] I want to be redirected to the thank you page after placing an order.
- [ ] I want to create a guest order.
- [ ] I want to select shipping address.
- [ ] I want to select billing address.
- [ ] I want to select a payment method.
- [ ] I want to select a shipping method.
- [ ] I want to apply coupon code.
- [ ] I want to proceed my payment with external service.
### Thank You Page

- [ ] I want to see the thank you page so I am sure the order was placed successfully.

### User Management

- [x] I want to login as a customer So I can access My Account details and continue shopping as a recognized user.
- [x] I want to logout.
- [ ] I want to register as a new customer So I can later log in to My Account.
- [ ] I want to reset the password So I can get a new one when I forgot the current one.

### Address Management

- [ ] I want to add a new address to the list of my addresses So later I can easily place the orders.
- [ ] I want to delete the existing address from the list of my addresses As I don't want to use it.
- [ ] I want to edit the details of my address So I can fix the eventual mistakes that I made.
- [ ] I want to mark the existing address as default shipping address So I do not have to choose it every order.
- [ ] I want to mark the existing address as default billing address So I do not have to choose it every order.
- [x] I want to see the history of my orders (list) So I can track the status of my shopping experiences.
- [x] I want to see the history of my orders (details) So I can track the status of my shopping experiences.

### Prices / Tax
- [ ] I want to see the prices in the right currency and with applied tax.
- [ ] I want to see applied taxes depending on the selected country / area so I can display price properly.

### Multistores / Currencies / I18n

- [x] I want to change the language of the shop so I can easily understand the content.
- [ ] I want to see translated STATIC content to the language that I set so I can finally read the site in the language that I know.
- [ ] I want to see translated DYNAMIC content to the language that I set so I can finally read the site in the language that I know.
- [ ] I want to change the currency.
- [ ] I want to change the country.

### SEO / SSR
- [x] I want to have pages pre-rendered on server-side.
- [ ] I want to have pretty urls.


## How to start?

1. Open  theme/nuxt.config.js 
2. Change this line, set the uri where is your Virto platform is running
```JS
//Set with the url where target VC platform is running. 
//The VSF/next application plays a reverse-proxy for all incoming graphql requests and proxy to specified url where vc platform is running.
//This is mandatory to avoid CORS issues and for more flexible  routing settings for VC platform endpoints.
const vcUpstreamEndpointUri = "https://admin-demo.virtocommerce.com";
```
   
3. Install all required dependencies:

```sh
yarn install
```

3. (optional) Then you can verify if everything works properly by building all three projects:

```sh
yarn build
```

4. If everything built properly, you can start creating your new integration with:

```sh
yarn dev
```
