In this project, let's built a **Nxt Trendz - E-Commerce Application** by applying the concepts I have learned till now.


**Prime User credentials**
  ```
   username: rahul
   password: rahul@2021
  ```

**Non-Prime User credentials**
  ```
   username: raja
   password: raja@2021
   ```

### Refer to the image below:

<br/>

<div style="text-align: center;">
  <video style="max-width:70%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12);outline:none;" loop="true" autoplay="autoplay" controls="controls" muted>
    <source src="https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-cart-features-output.mp4" type="video/mp4">
  </video>
</div>


The app have the following functionalities

- When an _unauthenticated user_ tries to access the **Home, Products or Cart** route, the page will be navigated to Login Route

- Following are the features implemented

  -When invalid credentials are provided in the login form and clicked on the Login button then the respective error message from the response will displayed.
  
  -When the username and password are provided correctly and clicked on the Login button then the page should navigate to **HomeRoute**.
  
  -When an undefined path is provided in the URL then the page navigate to the **NotFoundRoute**.
  
  -When the Logout button is clicked then the page  be navigated to the LoginRoute.
  
  -When an authenticated user opens the Products Route then an HTTP GET request should be made to **productsApiUrl** with query parameters `title_search`, `category`, and `rating` with initial values as **empty strings**.
  
- When a value is entered in the Search Input and the `Enter` button is clicked
  - Make an HTTP GET request to the URL productsApiUrl with `jwt_token` in the Cookies and query parameter `title_search` with value as the text entered in the         Search Input
  - Display _loader_ while fetching the response
  - After the data is fetched successfully, display the list of products received in the response

- When a **Category** is clicked
  - Make an HTTP GET request to the URL **productsApiUrl** with `jwt_token` in the Cookies and query parameter `category` with value as the id of the category           clicked
  - Display _loader_ while fetching the response
  - After the data is fetched successfully, display the list of products received in the response

- When a **Rating** is clicked
  - Make an HTTP GET request to the URL **productsApiUrl** with `jwt_token` in the Cookies and query parameter `rating` with value as the id of the rating clicked
  - Display _loader_ while fetching the response
  - After the data is fetched successfully, display the list of products received in the response

- When the **Clear Filters** button is clicked
  - All the filters applied should be reset to initial values
  - Make an HTTP GET request to the URL **productsApiUrl** with`jwt_token` in the Cookies and without any filters
  - Display _loader_ while fetching the response
  - After the data is fetched successfully, display the list of products received in the response

- When multiple filters are applied, then the HTTP GET request should be made with all the filters that are applied
  - For example: When the **Electronics** Category is clicked and rating **4 and above** is clicked the **productsApiUrl** will be as follows
  
- When an _authenticated user_ clicks on a product in the Products Route, then the page should be navigated to **Product Item Details** route.

- When the **Product Item Details** route is opened,
  - An HTTP GET request should be made to productDetailsApiUrl with `product id` as path parameter.
  - **_loader_** should be displayed while the HTTP request is fetching the data
  - After the HTTP request is successful, the response received should be displayed.
  - The quantity of the product should initially be 1.
  - The quantity of the product should be incremented by 1 when the plus icon is clicked.
  - The quantity of the product should be decremented by 1 when the minus icon is clicked.
  - The list of similar products should be displayed.

- When the **Product Item Details** route is opened, if the response received in the HTTP GET request returns the status as `404`, then the [Failure view](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-product-details-error-lg-output.png) should be displayed.

- When the **Continue Shopping** button in the [Failure view](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-product-details-error-lg-output.png) is     clicked, the page should be navigated to Products Route.

- When an _unauthenticated user_ tries to access the **Product Item Details** route, the page should be navigated to Login Route
 
- When an authenticated user tries to add the same product multiple times
  - The quantity of the product should be updated accordingly, and the count of the cart items in the header should be remained same

- The total amount and number of items in the cart should be displayed in the Cart Route

- In each cart item in the cart
    - The quantity of the product should be incremented by one when the plus icon is clicked
    - The quantity of the product should be decremented by one when the minus icon is clicked
    - When the quantity of the product is one and the minus icon is clicked, then the respective product should be removed from the cart
    - Based on the quantity of the product, the product price and the Cart Summary, i.e the total cost should be updated accordingly

- When an _authenticated user_ clicked on the remove button, Cart Item should be removed from the CartList

- When an _authenticated user_ clicked on the **Remove all** button, all the Cart Items should be removed from the cart and [EmptyCartView]                           (https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-cart-features-empty-cart-view.png) should be displayed

- The following are the keys used in the context object
  - `cartList` - this variable stores the cart items
  - `removeAllCartItems` - this function is used to remove all the cart items in the cart List
  - `addCartItem` - this function adds the cart item to the cart list
  - `removeCartItem` - this function removes the cart item from the cart list
  - `incrementCartItemQuantity` - this function increases the quantity of the product in the cart list
  - `decrementCartItemQuantity` - this function decreases the quantity of the product in the cart list


