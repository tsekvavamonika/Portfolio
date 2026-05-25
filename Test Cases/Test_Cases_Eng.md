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
