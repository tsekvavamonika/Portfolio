# Bug Report N1
## Password Reset – Email Link Sending Process

## Environment

| Parameter            | Details                                                          |
|----------------------|------------------------------------------------------------------|
| Test Device          | Laptop, VivoBook_ASUSLaptop X509JB_X509JB                       |
| Operating System     | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100         |
| Browser              | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit)  |
| Reproducibility Rate | 100%                                                             |

## Test Data

| Email Address        |
|----------------------|
| testUser@gmail.com   |

## Precondition
- The user is registered in the system
- The user is not authorized in the system

| **N** | **Steps**                                                                 | **Test Data**          |
|------|----------------------------------------------------------------------------|------------------------|
| 1    | Open the website https://.....ge/ka/                                       | -                      |
| 2    | Click the **“Authorization”** button in the header                         | -                      |
| 3    | Click the **“Forgot Password?”** button below the password input field     | -                      |
| 4    | Enter the registered email address                                         | testUser@gmail.com     |
| 5    | Click the **“Send Reset Link”** button                                     | -                      |

## Actual Result
The reset link is not sent to the email address, and the following error message appears:

> “An error occurred while sending the email.”

## Expected Result
The reset link is successfully sent, and the following message appears:

> “Password reset email has been sent successfully.”

## Attachment
Example

# Bug Report N2
## Logout & Re-login: Incorrect Cart and Wishlist Behavior After Logging Out from Checkout Page and Logging Back In

## Environment

| Parameter            | Details                                                          |
|----------------------|------------------------------------------------------------------|
| Test Device          | Laptop, VivoBook_ASUSLaptop X509JB_X509JB                       |
| Operating System     | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100         |
| Browser              | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit)  |
| Reproducibility Rate | 100%                                                             |

## Test Data

| Credentials               |
|---------------------------|
| Email: testUser2@gmail.com |
| Password: Test123!         |

## Precondition
- The user is authorized in the system.
- At least one product is added to the cart.
- At least one product is added to the wishlist.

## Steps to Reproduce

| **N** | **Steps**                                                                 | **Test Data** |
|------|----------------------------------------------------------------------------|----------------|
| 1    | Open the website https://......ge/ka/                                      | -              |
| 2    | Click the **“Bag”** button in the header                                   | -              |
| 3    | Click the **“Place Order”** button                                         | -              |
| 4    | On the logo page, click the profile initials button (T U)                  | -              |
| 5    | From the dropdown menu, click the **“Logout”** button                      | -              |
| 6    | Log in again using the same user account                                   | Email Address  |

## Actual Result
- After logout, the cart and wishlist are not cleared.
- After logging in again, the cart becomes empty, while the wishlist remains unchanged.

## Expected Result
- Both the cart and wishlist should be cleared after logout.
- After logging in again, the cart and wishlist should display and preserve the same items and quantities that the user had before logging out.

## Attachment
Example

# Bug Report N3
## Dropdown: On the “Vacancies” Page, the “Horeca” Category is Duplicated in the Categories Dropdown and Changes to Another Category After Refresh

## Environment

| Parameter            | Details                                                          |
|----------------------|------------------------------------------------------------------|
| Test Device          | Laptop, VivoBook_ASUSLaptop X509JB_X509JB                       |
| Operating System     | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100         |
| Browser              | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit)  |
| Reproducibility Rate | 100%                                                             |

## Steps to Reproduce

| **N** | **Steps**                                                                 | **Test Data** |
|------|----------------------------------------------------------------------------|----------------|
| 1    | Open the website https://......ge/ka/                                      | -              |
| 2    | Click the **“Vacancies”** button in the navbar                             | -              |
| 3    | In the filter bar, click the **“Category”** button                         | -              |
| 4    | Refresh the page                                                           | -              |

## Actual Result
- In the dropdown menu, the **“Horeca”** category is initially displayed twice.
- After refreshing the page, the second **“Horeca”** entry is replaced with the **“Hospitality”** category.

## Expected Result
- Each category should be displayed only once in the dropdown menu and should not change after refreshing the page.

## Attachment
Example

# Bug Report N4
## Filters: Color Icons Do Not Match Their Corresponding Color Names in the Color Filter

## Environment

| Parameter            | Details                                                          |
|----------------------|------------------------------------------------------------------|
| Test Device          | Laptop, VivoBook_ASUSLaptop X509JB_X509JB                       |
| Operating System     | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100         |
| Browser              | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit)  |
| Reproducibility Rate | 100%                                                             |

## Precondition
- The **“Men”** category catalog is open
- The system contains products in different colors

## Steps to Reproduce

| **N** | **Steps**                                                                 | **Test Data** |
|------|----------------------------------------------------------------------------|----------------|
| 1    | Open the website https://......ge/ka/                                      | -              |
| 2    | Scroll down to the color filters section                                   | -              |

## Actual Result
- In the color filter, the color names **Pink, Beige, Dark Blue, Green, Gray, Gold, Black & White, Yellow, Sky Blue** do not display matching color icons.
- A white icon is displayed by default instead.

## Expected Result
- Each color name in the color filter should display its corresponding color icon.

## Attachment
Example

# Bug Report N5

## Authentication: User Remains Authorized After Logout and Browser Refresh

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Precondition
- User is authorized in the system
- User account contains saved cart items

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | Open the website https://......ge/ka/ | - |
| 2 | Log in using a valid user account | testUser@gmail.com |
| 3 | Click the profile icon | - |
| 4 | Click the **“Logout”** button | - |
| 5 | Refresh the page | - |
| 6 | Try to access the user profile page directly | - |

## Actual Result
- After refreshing the page, the user remains partially authorized.
- The profile page is still accessible without re-login.

## Expected Result
- After logout, the session should be fully invalidated.
- Protected pages should no longer be accessible.

## Attachment
Example

# Bug Report N6

## Payment: Successful Payment Keeps Order Status as “Pending”

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Precondition
- User has products in cart

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | Proceed to checkout | - |
| 2 | Complete payment using a valid card | Test Visa Card |
| 3 | Open order history | - |

## Actual Result
- Payment is successful, but order status remains **“Pending”**.

## Expected Result
- Order status should update to **“Paid”** or **“Confirmed”** after successful payment.

## Attachment
Example

# Bug Report N7

## Cart: Duplicate Products Added After Double Clicking “Add to Cart” Button

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | Open a product details page | - |
| 2 | Double click the **“Add to Cart”** button quickly | - |
| 3 | Open the cart page | - |

## Actual Result
- Duplicate products are added to the cart.

## Expected Result
- Only one product should be added regardless of multiple quick clicks.

## Attachment
Example

# Bug Report N8

## Authorization: User Can Access Checkout Page Without Login

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | Logout from the system | - |
| 2 | Paste direct checkout URL into browser | /checkout |
| 3 | Press Enter | - |

## Actual Result
- Unauthorized user can access checkout page.

## Expected Result
- Unauthorized users should be redirected to the login page.

## Attachment
Example

# Bug Report N9

## Product Page: Out-of-Stock Product Can Still Be Purchased

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Precondition
- Product stock quantity equals 0

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | Open out-of-stock product page | - |
| 2 | Click the **“Add to Cart”** button | - |
| 3 | Proceed to checkout | - |

## Actual Result
- Out-of-stock product is successfully added to cart and can be purchased.

## Expected Result
- Out-of-stock products should not be purchasable.

## Attachment
Example

# Bug Report N10

## Checkout: Order Total Price Changes After Page Refresh

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Precondition
- User is authorized
- Cart contains multiple products

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | Open the website https://......ge/ka/ | - |
| 2 | Add multiple products to the cart | - |
| 3 | Proceed to checkout | - |
| 4 | Note the total price | - |
| 5 | Refresh the checkout page | - |

## Actual Result
- The total order price changes after refreshing the page.
- Discount calculation becomes incorrect.

## Expected Result
- The order total and discount values should remain unchanged after page refresh.

## Attachment
Example

# Bug Report N11

## Session Timeout: User Actions Still Available After Session Expiration

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Precondition
- User is authorized

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | Login into the system | testUser@gmail.com |
| 2 | Stay inactive until session expires | - |
| 3 | Try adding product to cart | - |

## Actual Result
- User can still perform actions after session expiration.

## Expected Result
- User should be redirected to login page after session expiration.

## Attachment
Example

