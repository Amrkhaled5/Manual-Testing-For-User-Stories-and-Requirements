# User Story 3: Contact Us

## Description
As a customer, I want to contact the website about a problem with my product so that I can receive assistance and support.

## Acceptance Criteria
1. Email address should be valid with the following structure (name@domain.xyz)
2. Email is a mandatory field
3. Contact name is a mandatory field
4. Message shouldn't be more than 500 characters
5. Message is a mandatory field

---

## Test Cases

### Positive Test Cases

| Test Case ID | Test Case Title | Pre-condition | Test Case Steps | Priority | Expected Results |
|--------------|-----------------|---------------|-----------------|----------|------------------|
| TC_001 | Validate contact with website using valid email and valid data | - Working software<br>- Valid customer data | 1. Open the app<br>2. Login as customer<br>3. Navigate to contact page<br>4. Enter valid name: "John Doe"<br>5. Enter valid email: "john.doe@test.com"<br>6. Enter message less than 500 characters<br>7. Click Send | High | - Message sent successfully<br>- Confirmation message displayed |
| TC_002 | Validate contact with website using valid data with message exactly 500 characters | - Working software<br>- Valid customer data | 1. Open the app<br>2. Login as customer<br>3. Navigate to contact page<br>4. Enter valid name: "John Doe"<br>5. Enter valid email: "john.doe@test.com"<br>6. Enter message with exactly 500 characters<br>7. Click Send | Medium | - Message sent successfully<br>- Confirmation message displayed |
| TC_003 | Validate contact with website using special characters in name and message | - Working software<br>- Valid customer data | 1. Open the app<br>2. Login as customer<br>3. Navigate to contact page<br>4. Enter name with special characters: "!John3@"<br>5. Enter valid email: "john.doe@test.com"<br>6. Enter message ≤ 500 chars with special characters<br>7. Click Send | Medium | - Message sent successfully<br>- Confirmation message displayed<br>- Special characters handled properly |

### Negative Test Cases

| Test Case ID | Test Case Title | Pre-condition | Test Case Steps | Priority | Expected Results |
|--------------|-----------------|---------------|-----------------|----------|------------------|
| TC_004 | Validate contact with website using invalid email format | - Working software<br>- Valid customer data | 1. Open the app<br>2. Login as customer<br>3. Navigate to contact page<br>4. Enter valid name: "John Doe"<br>5. Enter invalid email: "john.doe@test.c"<br>6. Enter message ≤ 500 characters<br>7. Click Send | High | - Error message: "Please enter a valid email"<br>- Message not sent |
| TC_005 | Validate contact with website without email | - Working software<br>- Valid customer data | 1. Open the app<br>2. Login as customer<br>3. Navigate to contact page<br>4. Enter valid name: "John Doe"<br>5. Leave email field empty<br>6. Enter message ≤ 500 characters<br>7. Click Send | High | - Error message: "Email field is required"<br>- Message not sent |
| TC_006 | Validate contact with website without name | - Working software<br>- Valid customer data | 1. Open the app<br>2. Login as customer<br>3. Navigate to contact page<br>4. Leave name field empty<br>5. Enter valid email: "john.doe@test.com"<br>6. Enter message ≤ 500 characters<br>7. Click Send | High | - Error message: "Name field is required"<br>- Message not sent |
| TC_007 | Validate contact with website without message | - Working software<br>- Valid customer data | 1. Open the app<br>2. Login as customer<br>3. Navigate to contact page<br>4. Enter valid name: "John Doe"<br>5. Enter valid email: "john.doe@test.com"<br>6. Leave message field empty<br>7. Click Send | High | - Error message: "Message field is required"<br>- Message not sent |
| TC_008 | Validate contact with website using message with more than 500 characters | - Working software<br>- Valid customer data | 1. Open the app<br>2. Login as customer<br>3. Navigate to contact page<br>4. Enter valid name: "John Doe"<br>5. Enter valid email: "john.doe@test.com"<br>6. Enter message with more than 500 characters<br>7. Click Send | High | - Error message: "Message should not exceed 500 characters"<br>- Message not sent |
| TC_009 | Validate contact with website with spaces in all fields | - Working software<br>- Valid customer data | 1. Open the app<br>2. Login as customer<br>3. Navigate to contact page<br>4. Enter name field with only spaces: "   "<br>5. Enter email field with only spaces: "   "<br>6. Enter message with only spaces<br>7. Click Send | Medium | - Error message: "Field cannot be empty"<br>- Message not sent |

## Test Data Requirements

### Valid Test Data
- **Valid Names**: "John Doe", "Mary Smith", "Ahmed Ali"
- **Valid Emails**: 
  - john.doe@example.com
  - mary.smith@test.org
  - ahmed.ali@company.co.uk
- **Valid Messages**: 
  - Short message (50 characters)
  - Medium message (250 characters)
  - Maximum length message (500 characters)

### Invalid Test Data
- **Invalid Emails**:
  - missing @ symbol: "userexample.com"
  - missing domain: "user@"
  - invalid domain: "user@test.c"
  - multiple @ symbols: "user@@example.com"
- **Invalid Messages**:
  - Over 500 characters: [501+ character string]
  - Empty string: ""
  - Only spaces: "     "



## Pre-test Checklist
1. Verify contact form is accessible
2. Check email server configuration
3. Ensure database logging is enabled
4. Clear browser cache and cookies
5. Prepare test data sets

## Post-test Activities
1. Verify submitted messages in database
2. Check email confirmations sent
3. Clean up test data
4. Review server logs for errors
5. Document any UI/UX observations