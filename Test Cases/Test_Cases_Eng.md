# Test Case N1
## Purchasing the Last Available Unit of the Same Product from Two Different Accounts

## Description
Verify transaction handling when two different users attempt to purchase the last available unit of the same product simultaneously.

## Precondition
- **User A** and **User B** are authorized in the system  
- Both users have the same product added to their carts:  
  - Product Name: Samsonite - RESTACKD 81/30  
  - Product stock quantity = 1  

## Post-condition
- **User A** successfully completes the order  
- **User B** cannot purchase the product and receives the error message: **“Product is out of stock”**  
- Product stock quantity in the system = 0  

## Single parameters

| Parameter | Details |
|--------------------------------|------------------------------------------------------|
| **User A - Account** | testUser1@gmail.com, Test123! |
| **User B - Account** | testUser2@gmail.com, Test123! |
| **User A - Card Details** | Card Number: 4111 1111 1111 1111<br>Expiration Date: 12/26<br>CVV: 123 |

## Steps to Reproduce

| **N** | **Steps** | **Test Data** | **Expected Result** |
|-------|-----------|----------------|----------------------|
| 1 | **User A** - Click the **“Bag”** button on the right side | - | A popup window is opened displaying:<ul><li>Product Name = Samsonite - RESTACKD 81/30</li><li>Product Quantity = 1</li><li>Total Amount = 1 099.00 ₾</li></ul> |
| 2 | **User A** - Click the **“Proceed to Checkout”** button | - | Checkout page is opened where:<ul><li>“Store Pickup” is selected by default</li><li>Address field is filled in</li><li>“Delivery” dropdown is opened and “Standard” is selected by default</li></ul> |
| 3 | **User B** - Click the **“Bag”** button on the right side | - | A popup window is opened displaying:<ul><li>Product Name = Samsonite - RESTACKD 81/30</li><li>Product Quantity = 1</li><li>Total Amount = 1 099.00 ₾</li></ul> |
| 4 | **User B** - Click the **“Proceed to Checkout”** button | - | Checkout page is opened where:<ul><li>“Store Pickup” is selected by default</li><li>Address field is filled in</li><li>“Delivery” dropdown is opened and “Standard” is selected by default</li></ul> |
| 5 | **User A and User B** - Select delivery time | **Within 3 Hours** | <ul><li>Delivery time is selected successfully</li><li>Delivery dropdown closes automatically</li><li>Payment dropdown is opened</li></ul> |
| 6 | **User A and User B** - Select payment method | **Bank of Georgia** | <ul><li>Payment bank is selected successfully</li><li>Payment dropdown closes automatically</li></ul> |
| 7 | **User A** - Click the **“Buy”** button | - | User is redirected to the bank payment page |
| 8 | **User A** - Select payment method | **Pay with Card** | Card payment form is opened displaying:<ul><li>Card Number field</li><li>Expiration Date field</li><li>CVV field</li></ul> |
| 9 | **User A** - Enter card details | **User A - Card Details** | <ul><li>Product purchase is completed successfully</li><li>Success message appears: **"You have successfully purchased the product"**</li></ul> |
| 10 | **User B** - Click the **“Buy”** button | - | <ul><li>Product purchase cannot be completed</li><li>Error message appears: **“Purchase failed, product is out of stock”**</li></ul> |

------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Test Case N2
## Verify Reducing Product Quantity in the Cart to the Minimum Invalid Value (0)

## Description
Verify the cart quantity management functionality and ensure that when the product quantity is reduced to 0, the cart becomes empty and the appropriate message is displayed.

## Precondition
- User is authorized in the system  
- Product Samsonite - RESTACKD 81/30 is added to the cart  
- Quantity = 1  

## Post-condition
- Product is removed from the cart  
- Message appears: **“There are no products left in your cart”**

## Single parameters

| Parameter | Details |
|--------------------------------|------------------------------------------------------|
| **User Account** | testUser@gmail.com, Test123! |

## Steps to Reproduce

| **N** | **Steps** | **Test Data** | **Expected Result** |
|-------|-----------|----------------|----------------------|
| 1 | Click the **“Bag”** button on the right side | - | A popup window is opened displaying:<ul><li>Product Name = Samsonite - RESTACKD 81/30</li><li>Product Quantity = 1</li><li>Total Amount = 1 099.00 ₾</li></ul> |
| 2 | Click the decrease arrow to reduce quantity (1 → 0) | - | Product quantity decreases but the product is still displayed |
| 3 | Wait for the UI to refresh | - | <ul><li>Product disappears from the cart</li><li>Message appears: **“There are no products left in your cart”**</li></ul> |

------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Test Case N3
## Verify Entering an Expired Promo Code

## Description
Verify that when an expired promo code is entered, the system does not apply the discount and displays the message: **“Promo code has expired”**.

## Precondition
- User is authorized in the system  
- Product Samsonite - RESTACKD 81/30 is added to the cart  
- Quantity = 1  

## Post-condition
- Product remains unchanged in the cart (without discount)  
- Order total remains the same (1 099.00 ₾)  
- Message appears: **“Promo code has expired”**

## Single parameters

| Parameter | Details |
|--------------------------------|------------------------------------------------------|
| **User Account** | testUser@gmail.com, Test123! |
| **Expired Promo Code** | Test123 |

## Steps to Reproduce

| **N** | **Steps** | **Test Data** | **Expected Result** |
|-------|-----------|----------------|----------------------|
| 1 | Click the **“Bag”** button on the right side | - | Cart popup window is opened |
| 2 | Click the **“Proceed to Checkout”** button | - | Checkout page is opened |
| 3 | In the **“Order Details”** section, click **“Promo Code & Gift Card”** | - | Promo code input field is opened |
| 4 | Enter the expired promo code and click **“Add”** | **Expired Promo Code** | <ul><li>Promo code is not applied</li><li>Message appears: **“Promo code has expired”**</li></ul> |

------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Test Case N4
## Verify Cart Persistence After Logout and Re-login

## Description
Verify that products added to the cart remain saved after logout and re-login.

## Precondition
- User is authorized in the system

## Post-condition
- Product remains in the cart after logout and re-login

## Single parameters

| Parameter | Details |
|--------------------------------|------------------------------------------------------|
| **User Account** | testUser2@gmail.com, Test123! |

## Steps to Reproduce

| **N** | **Steps** | **Test Data** | **Expected Result** |
|-------|-----------|----------------|----------------------|
| 1 | Enter **"პროდიჟიოზი პარფიუმი ფლორალი 50მლ"** in the search field | - | Relevant product appears in search results |
| 2 | Click the product | - | Product details page is opened |
| 3 | Click the **“Add to Cart”** button | - | Product is successfully added to the cart |
| 4 | Close the cart popup | - | Popup is successfully closed |
| 5 | Click your name near the profile icon | - | Profile dropdown menu appears |
| 6 | Click the **“Logout”** button | - | User is successfully logged out |
| 7 | Log in again using the same account | **User Account** | User is successfully logged in |
| 8 | Open the cart | - | Previously added product is still displayed in the cart |

------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Test Case N5
## Verify Product Filtering with an Invalid Price Range (min > max)

## Description
Verify system behavior when the minimum price is greater than the maximum price. The system should automatically correct the filter values.

## Precondition
- The **“Men”** category catalog is opened  
- Products with different prices exist in the system

## Post-condition
- System automatically corrects filter values: min = max  
- Products within the specified range are displayed

# Test Case N5
## Verify Product Filtering with an Invalid Price Range (min > max)

## Description
Verify system behavior when the minimum price is greater than the maximum price. The system should automatically correct the filter values.

## Precondition
- The **“Men”** category catalog is opened  
- Products with different prices exist in the system

## Post-condition
- System automatically corrects filter values: min = max  
- Products within the specified range are displayed

## Steps to Reproduce

| **N** | **Steps** | **Test Data** | **Expected Result** |
|-------|-----------|----------------|----------------------|
| 1 | Scroll down to the price filter section | - | <ul><li>Price slider and Min/Max input fields are displayed</li><li>Current default minimum and maximum prices are displayed in the UI</li></ul> |
| 2 | Enter the minimum price value in the left input field | **20** | Minimum price field accepts the value 20 |
| 3 | Press **Enter** | - | <ul><li>The left side of the slider updates</li><li>Products matching the minimum price filter are displayed</li></ul> |
| 4 | Enter a maximum price value lower than the minimum value | **19** | Maximum price field temporarily accepts the value 19 |
| 5 | Press **Enter** | - | <ul><li>System automatically corrects the range: Min = 20, Max = 20</li><li>Slider updates to the correct position</li><li>Product list refreshes accordingly</li></ul> |

------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Test Case N6
## Verify Password Reset Email Link Sending Process

## Description
Verify proper functionality of the password reset feature and ensure that a password reset link is successfully sent to the user’s email address.

## Precondition
- User is registered in the system  
- User has a valid email address linked to the account

## Post-condition
- Active password reset link is generated in the system  
- Password reset link is successfully sent to the email address  
- User sees a success confirmation message

## Single parameters

| Parameter | Details |
|--------------------------------|------------------------------------------------------|
| **User Email** | testUser@gmail.com |

## Steps to Reproduce

| **N** | **Steps** | **Test Data** | **Expected Result** |
|-------|-----------|----------------|----------------------|
| 1 | Click the **“Authorization”** button in the top right corner | - | Authorization popup window is opened |
| 2 | Click the **“Forgot Password?”** button | - | Password recovery page is opened |
| 3 | Enter the registered email address | **User Email** | <ul><li>Password reset link is successfully sent</li><li>Success confirmation message is displayed</li></ul> |

------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Test Case N7
## Verify Direct Access to Checkout Page After Logout Using URL

## Description
Verify that an unauthorized user cannot access the Checkout page using a direct URL after logout.

## Precondition
- User is authorized in the system

## Post-condition
- User is redirected to the authorization page  
- Checkout page is not accessible for unauthorized users

## Single parameters

| Parameter | Details |
|--------------------------------|------------------------------------------------------|
| **Checkout URL** | https://......ge/checkout |

## Steps to Reproduce

| **N** | **Steps** | **Test Data** | **Expected Result** |
|-------|-----------|----------------|----------------------|
| 1 | Click the profile icon on the right side | - | Profile dropdown menu appears |
| 2 | Click the **“Logout”** button | - | User is successfully logged out |
| 3 | Paste the Checkout page URL into the browser address bar | **Checkout URL** | URL is entered successfully |
| 4 | Press **Enter** | - | <ul><li>User is redirected to the authorization page</li><li>Checkout page is not opened</li></ul> |

------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Test Case N8
## Verify Adding an Out-of-Stock Product to the Cart

## Description
Verify that an out-of-stock product cannot be added to the cart.

## Precondition
- Product stock quantity = 0  
- User is authorized in the system

## Post-condition
- Product is not added to the cart  
- User sees an appropriate error message

## Single parameters

| Parameter | Details |
|--------------------------------|------------------------------------------------------|
| **Product Name** | Samsonite - RESTACKD 81/30 |

## Steps to Reproduce

| **N** | **Steps** | **Test Data** | **Expected Result** |
|-------|-----------|----------------|----------------------|
| 1 | Open the product details page | **Product Name** | Product details page is opened |
| 2 | Click the **“Add to Cart”** button | - | <ul><li>Product is not added to the cart</li><li>Error message appears: **"Product is out of stock"**</li></ul> |
| 3 | Open the cart | - | Product is not displayed in the cart |

------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Test Case N9
## Verify Order Total After Refreshing the Checkout Page

## Description
Verify that the order total and discount values remain unchanged after refreshing the Checkout page.

## Precondition
- User is authorized in the system  
- Multiple products are added to the cart

## Post-condition
- Order total remains unchanged  
- Discount value remains unchanged

## Single parameters

| Parameter | Details |
|--------------------------------|------------------------------------------------------|
| **Product Quantity** | 3 |

## Steps to Reproduce

| **N** | **Steps** | **Test Data** | **Expected Result** |
|-------|-----------|----------------|----------------------|
| 1 | Add multiple products to the cart | **3** | Products are successfully added to the cart |
| 2 | Click the **“Proceed to Checkout”** button | - | Checkout page is opened |
| 3 | Note the total order amount | - | Total order amount and discount are displayed |
| 4 | Refresh the page | - | Checkout page reloads successfully |
| 5 | Verify the order details | - | <ul><li>Total order amount remains unchanged</li><li>Discount value remains unchanged</li></ul> |

------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Test Case N10
## Verify Multiple Rapid Clicks on the “Add to Cart” Button

## Description
Verify that rapidly clicking the “Add to Cart” button multiple times adds the product to the cart only once.

## Precondition
- User is authorized in the system  
- Product is available in stock

## Post-condition
- Product is added to the cart only once

## Single parameters

| Parameter | Details |
|--------------------------------|------------------------------------------------------|
| **Product Name** | Samsonite - RESTACKD 81/30 |

## Steps to Reproduce

| **N** | **Steps** | **Test Data** | **Expected Result** |
|-------|-----------|----------------|----------------------|
| 1 | Open the product details page | **Product Name** | Product details page is opened |
| 2 | Rapidly click the **“Add to Cart”** button multiple times | - | UI responds to multiple clicks |
| 3 | Open the cart | - | <ul><li>Product is added only once</li><li>Quantity = 1</li></ul> |

------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Test Case N11
## Verify User Actions After Session Expiration

## Description
Verify that the user cannot perform actions after the session has expired.

## Precondition
- User is authorized in the system

## Post-condition
- User is redirected to the authorization page  
- User actions are no longer available in the system

## Single parameters

| Parameter | Details |
|--------------------------------|------------------------------------------------------|
| **User Account** | testUser@gmail.com, Test123! |

## Steps to Reproduce

| **N** | **Steps** | **Test Data** | **Expected Result** |
|-------|-----------|----------------|----------------------|
| 1 | Log in to the system | **User Account** | User is successfully logged into the system |
| 2 | Stay inactive until the session expires | - | Session timeout occurs |
| 3 | Try adding a product to the cart | - | <ul><li>User is redirected to the authorization page</li><li>Product is not added to the cart</li></ul> |
