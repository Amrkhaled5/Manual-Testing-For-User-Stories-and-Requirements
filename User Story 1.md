# User Story 1: Open a Credit Card Account

## Description
As a customer, I want to open a credit card account to receive appropriate discounts based on my customer status and available promotions.

## Acceptance Criteria
1. First-time customers get 15% discount on all purchases today
2. Existing customers with loyalty cards get 10% discount
3. Customers with coupons get 20% discount (cannot be combined with new customer discount)
4. Discount amounts are added when applicable

---

## Test Cases

### Positive Test Cases

| Test Case ID | Test Case Title | Pre-condition | Test Case Steps | Priority | Expected Results |
|--------------|-----------------|---------------|-----------------|----------|------------------|
| TC_001 | Validate discount for existing customer with no loyalty or coupon | - Working software<br>- Valid existing customer data<br>- Valid credit card with funds<br>- Items available in cart | 1. Open the app as customer<br>2. Sign in with existing customer data<br>3. Add items to cart<br>4. Checkout with Credit Card<br>5. Fill all required card data<br>6. Click Confirm | Medium | - No discount applied<br>- Transaction completes successfully |
| TC_002 | Validate discount for new customer | - Working software<br>- Valid new customer data<br>- Valid credit card with funds<br>- Items available in cart | 1. Open the app as customer<br>2. Register as new Customer<br>3. Add items to cart<br>4. Checkout with Credit Card<br>5. Fill all required card data<br>6. Click Confirm | High | - 15% discount applied for total amount<br>- Discount appears before clicking Buy |
| TC_003 | Validate discount for existing customer with loyalty card | - Working software<br>- Existing customer data<br>- Valid loyalty card<br>- Items available in cart | 1. Open the app as customer<br>2. Sign in with existing customer data<br>3. Add items to cart<br>4. Checkout with Credit Card<br>5. Fill all required card data<br>6. Click Confirm | High | - 10% discount applied for total amount<br>- Discount appears before clicking Buy |
| TC_004 | Validate discount for existing customer with coupon | - Working software<br>- Existing customer data<br>- Valid credit card with funds<br>- Items available in cart<br>- Valid coupon | 1. Open the app as customer<br>2. Sign in with existing customer data<br>3. Add items to cart<br>4. Checkout with Credit Card<br>5. Fill all required card data<br>6. Enter coupon data<br>7. Click Confirm | High | - 20% discount applied for total amount<br>- Discount appears before clicking Buy |
| TC_005 | Validate discount for existing customer with loyalty card and valid coupon | - Working software<br>- Existing customer with loyalty card<br>- Valid credit card with funds<br>- Items available in cart<br>- Valid coupon | 1. Open the app as customer<br>2. Sign in with existing customer data<br>3. Add items to cart<br>4. Checkout with Credit Card<br>5. Fill all required card data<br>6. Enter coupon data<br>7. Click Confirm | High | - 30% total discount applied (10% loyalty + 20% coupon)<br>- Combined discount appears before clicking Buy |
| TC_006 | Validate discount for new customer with valid coupon | - Working software<br>- Valid new customer data<br>- Valid credit card with funds<br>- Items available in cart<br>- Valid coupon | 1. Open the app as customer<br>2. Register as new Customer<br>3. Add items to cart<br>4. Checkout with Credit Card<br>5. Fill all required card data<br>6. Enter coupon data<br>7. Click Confirm | High | - 20% discount applied for total amount<br>- New customer discount should not be added to coupon discount |

### Negative Test Cases

| Test Case ID | Test Case Title | Pre-condition | Test Case Steps | Priority | Expected Results |
|--------------|-----------------|---------------|-----------------|----------|------------------|
| TC_007 | Validate discount for new customer with loyalty card and valid coupon | - Working software<br>- Valid new customer data<br>- Valid loyalty card<br>- Valid coupon<br>- Items available in cart | 1. Open the app as customer<br>2. Register as new Customer<br>3. Add items to cart<br>4. Checkout with Credit Card<br>5. Fill all required card data<br>6. Enter coupon data<br>7. Click Confirm | Medium | - Only 20% coupon discount applied<br>- Loyalty and new customer discounts ignored |
| TC_008 | Validate invalid or expired coupon for any user | - Working software<br>- Valid customer data (new or existing)<br>- Invalid or expired coupon<br>- Items available in cart | 1. Open the app as customer<br>2. Register/Sign in as Customer<br>3. Add items to cart<br>4. Checkout with Credit Card<br>5. Fill all required card data<br>6. Enter invalid/expired coupon data<br>7. Click Confirm | Medium | - Error: "Invalid or expired coupon"<br>- No discount added |
| TC_009 | Validate invalid or expired loyalty card for any user | - Working software<br>- Valid customer data<br>- Invalid or expired loyalty card<br>- Items available in cart | 1. Open the app as customer<br>2. Sign in with customer data<br>3. Add items to cart<br>4. Checkout with Credit Card<br>5. Fill all required card data<br>6. Enter invalid/expired loyalty card<br>7. Click Confirm | Medium | - Error: "Invalid loyalty card"<br>- No discount added |

---

## Test Data Requirements

### Valid Customer Data
- Existing customer: Email, password, customer ID
- New customer: Name, email, phone, address details

### Valid Credit Cards
- Card number: 4111111111111111 (Visa test card)
- Expiry: Future date (MM/YY format)
- CVV: 123
- Cardholder name: Test User

### Valid Coupons
- SAVE20: 20% discount coupon
- WELCOME15: 15% discount for new customers
- LOYALTY10: 10% loyalty discount

### Invalid Test Data
- Expired coupon: EXPIRED2023
- Invalid loyalty card: INVALID123
- Expired credit card: 12/22
