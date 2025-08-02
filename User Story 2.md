# User Story 2: Add Product to Cart

## Description
As a customer, I want to add a product to my cart so that I can purchase the product.

## Acceptance Criteria
1. Product should have at least one item to be added to the cart
2. If product is out of stock, user cannot add it to the cart
3. User clicks on "add to cart" button to add the product to the cart
4. A message is displayed to the user to inform that the product is added to the cart
5. There is a link in the notification message to redirect the user to the cart
6. The user should be logged in to be able to add to the cart

---

## Test Cases

### Positive Test Cases

| Test Case ID | Test Case Title | Pre-condition | Test Case Steps | Priority | Expected Results |
|--------------|-----------------|---------------|-----------------|----------|------------------|
| TC_001 | Validate add product to cart when stock is one or more | - Working software<br>- Valid customer data<br>- Product has stock quantity ≥ 1 | 1. Open the app<br>2. Login as customer<br>3. Navigate to product with valid stock<br>4. Click "Add to Cart" | High | - Product added to the cart<br>- Success message appears with link to navigate to cart |
| TC_002 | Validate add product to cart with just one item in stock | - Working software<br>- Valid customer data<br>- Product has exactly one item in stock | 1. Open the app<br>2. Login as customer<br>3. Navigate to product with one item in stock<br>4. Click "Add to Cart" | High | - Product added to the cart<br>- Success message appears with link to navigate to cart<br>- Stock becomes 0 |
| TC_003 | Validate add to cart notification and link functionality | - Working software<br>- Valid customer data<br>- Product has stock quantity ≥ 1 | 1. Open the app<br>2. Login as customer<br>3. Navigate to product with valid stock<br>4. Click "Add to Cart"<br>5. Click on the link in the success message | High | - Product added to the cart<br>- Success message appears with link<br>- Clicking link navigates user to the cart page |
| TC_004 | Validate adding the same product to cart multiple times | - Working software<br>- Valid customer data<br>- Product has stock quantity > 1 | 1. Open the app<br>2. Login as customer<br>3. Navigate to product with valid stock<br>4. Click "Add to Cart"<br>5. Repeat steps 3-4 multiple times with same product | Medium | - Product quantity increases each time<br>- Success message appears with link for each addition |
| TC_005 | Validate adding different products to cart with valid stock | - Working software<br>- Valid customer data<br>- All products have stock quantity ≥ 1 | 1. Open the app<br>2. Login as customer<br>3. Navigate to first product with valid stock<br>4. Click "Add to Cart"<br>5. Navigate to different product with valid stock<br>6. Click "Add to Cart"<br>7. Repeat for multiple different products | Medium | - All products added to the cart<br>- Success message appears with link for each product addition |

### Negative Test Cases

| Test Case ID | Test Case Title | Pre-condition | Test Case Steps | Priority | Expected Results |
|--------------|-----------------|---------------|-----------------|----------|------------------|
| TC_006 | Validate add product to cart without stock | - Working software<br>- Valid customer data<br>- Product has no stock (quantity = 0) | 1. Open the app<br>2. Login as customer<br>3. Navigate to product without stock<br>4. Click "Add to Cart" | High | - Product not added to the cart<br>- Error message appears: "Product is out of stock" |
| TC_007 | Validate add product to cart without being logged in | - Working software<br>- Product has stock quantity ≥ 1<br>- User not logged in | 1. Open the app<br>2. Navigate to product with valid stock<br>3. Click "Add to Cart" | High | - Product not added to the cart<br>- Error message appears: "You should log in"<br>- User redirected to login page |


## Test Data Requirements

### Valid Customer Data
- Username: testuser@example.com
- Password: TestPass123
- Customer ID: CUST001

### Product Test Data
- Product with stock: "Laptop" (Quantity: 10)
- Product with one item: "Limited Edition Watch" (Quantity: 1)
- Product out of stock: "Sold Out Phone" (Quantity: 0)
- High stock product: "Basic T-Shirt" (Quantity: 100)


## Pre-test Setup
1. Ensure test database has products with various stock levels
2. Create test customer accounts
3. Clear browser cache and cookies
4. Verify shopping cart functionality is enabled
5. Check network connectivity

## Post-test Cleanup
1. Clear shopping carts
2. Reset product stock quantities
3. Remove test data
4. Clear browser sessions