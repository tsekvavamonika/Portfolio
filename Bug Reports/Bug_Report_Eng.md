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

