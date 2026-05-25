# Bug Report N1
## პაროლის აღდგენა – მეილზე ბმულის გაგზავნის პროცესი

## Environment

| Parameter           | Details                                                        |
|---------------------|----------------------------------------------------------------|
| Test Device         | Laptop, VivoBook_ASUSLaptop X509JB_X509JB                     |
| Operating System    | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100      |
| Browser             | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100%                                                         |

## Test Data

| Email Address                  |
|----------------------------------|
| testUser@gmail.com   |


## Precondition
- მომხმარებელი რეგისტრირებულია სისტემაში  
- მომხმარებელი არ არის ავტორიზებული სისტემაში  



| **N** | **Steps**                                                                                     | **Test Data**                     |
|-------|------------------------------------------------------------------------------------------------|------------------------------------|
| 1     | გახსენით ვებსაიტი https://.....ge/ka/                                                     | -                                  |
| 2     | დააჭირეთ ჰედერში ღილაკს **“ავტორიზაცია”**                                                     | -                                  |
| 3     | დააჭირეთ ღილაკს **“დაგავიწყდა პაროლი?”** პაროლის ინფუთის ქვევით                               | -                                  |
| 4     | შეიყვანეთ თქვენი რეგისტრირებული ელფოსტა                                                       | testUser@gmail.com    |
| 5     | დააჭირეთ ღილაკს **"გადატვირთვის ბმულის გაგზავნა"**             | -                                  |
## Actual Result
ბმული არ იგზავნება მეილზე, ჩნდება შეცდომის შეტყობინება:  
> “An error occurred while sending the email.”

## Expected Result
ბმული გაიგზავნა და ჩნდება შეტყობინება:  
> “Password reset email has been sent successfully.”

## Attachment
Example

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Bug Report N2
## Logout & Re-login: Checkout გვერდიდან გამოსვლისას და ხელახლა შესვლისას კალათისა და სურვილების სიის არასწორი მუშაობა

## Environment

| Parameter           | Details                                                        |
|---------------------|----------------------------------------------------------------|
| Test Device         | Laptop, VivoBook_ASUSLaptop X509JB_X509JB                     |
| Operating System    | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100      |
| Browser             | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100%                                                         |


## Test Data

| Email Address                  |
|----------------------------------|
| email: testUser2@gmail.com |
| password: Test123!   |


## Precondition
- მომხმარებელი ავტორიზებულია სისტემაში.  
- კალათში არის მინიმუმ ერთი პროდუქტი.
- სურვილების სიაში არის მინიმუმ ერთი პროდუქტი.


## Steps to Reproduce

| **N** | **Steps**                                                                                     | **Test Data**                     |
|-------|------------------------------------------------------------------------------------------------|------------------------------------|
| 1     | გახსენით ვებსაიტი https://......ge/ka/                                                     | -                                  |
| 2     | ჰედერში დააჭირეთ ღილაკს **“ჩანთა“**                                                           | -                                  |
| 3     | დააჭირეთ ღილაკს **„შეკვეთის განთავსება“**                                                     | -                                  |
| 4     | ლოგოს გვერდზე დააჭირეთ პროფილის ინიციალების ღილაკს (T U)                                     | -                                  |
| 5     | Dropdown მენიუდან დააჭირეთ ღილაკს **„გამოსვლა“**                                              | -                                  |
| 6     | ხელახლა შედით იმავე მომხმარებლის ანგარიშით                                                   | **Email Address**    |

## Actual Result
- Logout-ის შესრულების შემდეგ კალათა და სურვილების სია არ სუფთავდება.  
- ხელახლა შესვლის შემდეგ კალათა ცარიელია, ხოლო სურვილების სია უცვლელი რჩება.

## Expected Result
- სისტემიდან გამოსვლისას სუფთავდება როგორც კალათი, ისე სურვილების სია.  
- ხელახლა შესვლისას სურვილების სიაში და ჩანთაში ნაჩვენებია და შენარჩუნებულია ის ნივთები და რაოდენობა, რაც მომხმარებელს ჰქონდა სისტემიდან გამოსვლამდე.

## Attachment
Example

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Bug Report N3

## Dropdown: „ვაკანსიების“ გვერდზე "კატეგორიების" დროფდაუნში - „ჰორეკა“ დუბლირდება, რეფრეშის შემდეგ კი იცვლება სხვა კატეგორიით.

## Environment

| Parameter           | Details                                                        |
|---------------------|----------------------------------------------------------------|
| Test Device         | Laptop, VivoBook_ASUSLaptop X509JB_X509JB                     |
| Operating System    | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100      |
| Browser             | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100%                                                         |

## Steps to Reproduce

| **N** | **Steps**                                                                                     | **Test Data**                     |
|-------|------------------------------------------------------------------------------------------------|------------------------------------|
| 1     | გახსენით ვებსაიტი https://......ge/ka/                                                     | -                                  |
| 2     | ჰნავბარში დააჭირეთ ღილაკს **„ვაკანსიები“**.                                                          | -                                  |
| 3     | Filter bar-ში(ფილტრების ზოლი) დააჭირეთ ღილაკს **„კატეგორია“**.                                              | -                                  |
| 4     | განაახლეთ გვერდი **(Refresh)**.                                   | -                                  |

## Actual Result
- დროფდაუნ მენიუში თავდაპირველად კატეგორია **„ჰორეკა“** ნაჩვენებია ორჯერ. რეფრეშის შემდეგ მეორე **„ჰორეკა“** - ჩანაცვლდება კატეგორიით **„სტუმართმოყვარეობა“**.

## Expected Result
- დროფდაუნ მენიუში, თითოეული კატეგორია უნდა გამოჩნდეს მხოლოდ ერთხელ და არ უნდა იცვლებოდეს გვერდის განახლების შემდეგ.

## Attachment
Example

# Bug Report N4
## Filters: ფერების ფილტრში - ფერის აიქონი არ შეესაბამება მის სახელწოდებებს

## Environment

| Parameter           | Details                                                        |
|---------------------|----------------------------------------------------------------|
| Test Device         | Laptop, VivoBook_ASUSLaptop X509JB_X509JB                     |
| Operating System    | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100      |
| Browser             | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100%                                                         |

## Precondition
- გახსნილია კატეგორია **“კაცი”**-ს კატალოგი
- სისტემაში არის სხვადასხვა ფერის პროდუქტი

## Steps to Reproduce

| **N** | **Steps**                                                                                     | **Test Data**                     |
|-------|------------------------------------------------------------------------------------------------|------------------------------------|
| 1     | გახსენით ვებსაიტი https://......ge/ka/                                                     | -                                  |
| 2     | ჩამოსქროლეთ ფერების ფილტრამდე.                                                          | -                                  |


## Actual Result
-  ფერების ფილტრში სიტყვებთან **ვარდისფერი, კრემისფერი, მუქი ლურჯი, მწვანე, ნაცრისფერი, ოქროსფერი, შავთეთრი, ყვითელი, ცისფერი** არ არის შესაბამისი ფერის აიქონი, Default-ად არის თეთრი.

## Expected Result
-  ფერების ფილტრში თითოეული ფერის სახელწოდებასთან უნდა იყოს ნაჩვენები შესაბამისი ფერის აიქონი.

## Attachment
Example

# Bug Report N5

## Authentication: სისტემიდან გამოსვლისა და გვერდის რეფრეშის შემდეგ მომხმარებელი კვლავ ავტორიზებულია

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Precondition
- მომხმარებელი ავტორიზებულია სისტემაში
- მომხმარებლის ანგარიშზე შენახულია პროდუქტები კალათაში

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | გახსენით ვებსაიტი https://......ge/ka/ | - |
| 2 | შედით სისტემაში ვალიდური ანგარიშით | testUser@gmail.com |
| 3 | დააჭირეთ პროფილის აიქონს | - |
| 4 | დააჭირეთ ღილაკს **“Logout”** | - |
| 5 | განაახლეთ გვერდი | - |
| 6 | სცადეთ პროფილის გვერდზე პირდაპირი გადასვლა | - |

## Actual Result
- გვერდის განახლების შემდეგ მომხმარებელი ნაწილობრივ კვლავ ავტორიზებულია.
- პროფილის გვერდი ხელმისაწვდომია ხელახლა ავტორიზაციის გარეშე.

## Expected Result
- Logout-ის შემდეგ სესია სრულად უნდა გაუქმდეს.
- დაცული გვერდები აღარ უნდა იყოს ხელმისაწვდომი.

## Attachment
Example

# Bug Report N6

## Payment: წარმატებული გადახდის შემდეგ შეკვეთის სტატუსი რჩება “Pending”

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Precondition
- მომხმარებლის კალათაში დამატებულია პროდუქტები

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | გადადით Checkout გვერდზე | - |
| 2 | შეასრულეთ გადახდა ვალიდური ბარათით | Test Visa Card |
| 3 | გახსენით შეკვეთების ისტორია | - |

## Actual Result
- გადახდა წარმატებით სრულდება, თუმცა შეკვეთის სტატუსი რჩება **“Pending”**.

## Expected Result
- წარმატებული გადახდის შემდეგ შეკვეთის სტატუსი უნდა შეიცვალოს **“Paid”** ან **“Confirmed”** მნიშვნელობით.

## Attachment
Example

# Bug Report N7

## Cart: “Add to Cart” ღილაკზე ორმაგი დაკლიკების შემდეგ პროდუქტი დუბლირდება

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
| 1 | გახსენით პროდუქტის დეტალური გვერდი | - |
| 2 | სწრაფად ორჯერ დააჭირეთ ღილაკს **“Add to Cart”** | - |
| 3 | გახსენით კალათა | - |

## Actual Result
- კალათაში ემატება დუბლირებული პროდუქტები.

## Expected Result
- რამდენჯერმე სწრაფი დაკლიკების მიუხედავად, პროდუქტი კალათაში მხოლოდ ერთხელ უნდა დაემატოს.

## Attachment
Example

# Bug Report N8

## Authorization: არაავტორიზებულ მომხმარებელს შეუძლია Checkout გვერდზე გადასვლა

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
| 1 | გამოდით სისტემიდან | - |
| 2 | ბრაუზერში ჩასვით Checkout გვერდის პირდაპირი URL | /checkout |
| 3 | დააჭირეთ Enter | - |

## Actual Result
- არაავტორიზებულ მომხმარებელს შეუძლია Checkout გვერდზე წვდომა.

## Expected Result
- არაავტორიზებული მომხმარებელი უნდა გადამისამართდეს ავტორიზაციის გვერდზე.

## Attachment
Example

# Bug Report N9

## Product Page: მარაგში არარსებული პროდუქტის შეძენა კვლავ შესაძლებელია

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Precondition
- პროდუქტის მარაგის რაოდენობა არის 0

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | გახსენით პროდუქტის გვერდი, რომელიც არ არის მარაგში | - |
| 2 | დააჭირეთ ღილაკს **“Add to Cart”** | - |
| 3 | გადადით Checkout გვერდზე | - |

## Actual Result
- მარაგში არარსებული პროდუქტი წარმატებით ემატება კალათაში და შესაძლებელია მისი შეძენა.

## Expected Result
- მარაგში არარსებული პროდუქტის შეძენა შეუძლებელი უნდა იყოს.

## Attachment
Example

# Bug Report N10

## Checkout: გვერდის განახლების შემდეგ შეკვეთის ჯამური თანხა იცვლება

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Precondition
- მომხმარებელი ავტორიზებულია
- კალათაში დამატებულია რამდენიმე პროდუქტი

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | გახსენით ვებსაიტი https://......ge/ka/ | - |
| 2 | დაამატეთ რამდენიმე პროდუქტი კალათაში | - |
| 3 | გადადით Checkout გვერდზე | - |
| 4 | დააკვირდით შეკვეთის ჯამურ თანხას | - |
| 5 | განაახლეთ Checkout გვერდი | - |

## Actual Result
- გვერდის განახლების შემდეგ შეკვეთის ჯამური თანხა იცვლება.
- ფასდაკლების გამოთვლა ხდება არასწორად.

## Expected Result
- გვერდის განახლების შემდეგ შეკვეთის ჯამური თანხა და ფასდაკლება უცვლელი უნდა დარჩეს.

## Attachment
Example

# Bug Report N11

## Session Timeout: სესიის ვადის გასვლის შემდეგ მომხმარებელს კვლავ შეუძლია მოქმედებების შესრულება

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Precondition
- მომხმარებელი ავტორიზებულია

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | შედით სისტემაში | testUser@gmail.com |
| 2 | არ შეასრულოთ მოქმედებები სესიის ვადის გასვლამდე | - |
| 3 | სცადეთ პროდუქტის კალათაში დამატება | - |

## Actual Result
- სესიის ვადის გასვლის შემდეგ მომხმარებელს კვლავ შეუძლია მოქმედებების შესრულება.

## Expected Result
- სესიის ვადის გასვლის შემდეგ მომხმარებელი უნდა გადამისამართდეს ავტორიზაციის გვერდზე.

## Attachment
Example
