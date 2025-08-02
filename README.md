# Test Cases Repository

This repository contains comprehensive test cases and documentation for various software testing scenarios across different domains and applications.

## 📋 Overview

This collection includes detailed test cases for multiple user stories and features, covering both positive and negative testing scenarios with complete test data requirements and execution guidelines.

## 📊 Master Test Cases Sheet

**[View Master Test Cases Spreadsheet](https://docs.google.com/spreadsheets/d/1Z6eJqYKzLyyT2YYm6craCnRmbEVZwuqC1PU_OChDuAo/edit?usp=sharing)**

The master spreadsheet contains all test cases in a structured format with the following columns:
- Test Case ID
- Test Case Title
- Pre-conditions
- Test Case Steps
- Priority Level
- Expected Results
- Questions and Notes

## 📁 Repository Contents

### 1. User Story 1: Credit Card Account & Discount System
**File:** `User Story 1.md`

Test cases for credit card account opening with dynamic discount system including:
- New customer discounts (15%)
- Loyalty card discounts (10%)
- Coupon-based discounts (20%)
- Combined discount scenarios
- Invalid coupon/loyalty card handling

**Key Features Tested:**
- Customer registration and authentication
- Discount calculation logic
- Payment processing
- Error handling for invalid promotions

### 2. User Story 2: Add Product to Cart
**File:** `User Story 2.md`

Comprehensive test cases for e-commerce cart functionality covering:
- Adding products with available stock
- Out-of-stock product handling
- User authentication requirements
- Cart notification system
- Multiple product scenarios

**Key Features Tested:**
- Stock management validation
- User session handling
- Cart state management
- Success/error messaging

### 3. User Story 3: Contact Us Form
**File:** `User Story 3.md`

Test cases for customer support contact form with validation rules:
- Email format validation (name@domain.xyz)
- Mandatory field requirements
- Message length constraints (≤500 characters)
- Special character handling
- Form submission workflows

**Key Features Tested:**
- Input validation and sanitization
- Form field requirements
- Character limit enforcement
- Error message display

### 4. Quiz Game Feature
**File:** `Quiz Game.md`

Test cases for subscription-based quiz game functionality:
- 5-question quiz structure
- Text and image-based answer options
- Subscription validation
- Reward system for successful completion
- Progress tracking and retry functionality

**Key Features Tested:**
- Subscription access control
- Game flow and logic
- Reward distribution
- User progress tracking

### 5. Aviation Portal Booking System
**File:** `Aviation Portal.md`

Complex test cases for flight booking portal with specific discount conditions:
- Time-bound discount offers (Dec 15-18, 2018 booking period)
- Geographic restrictions (Cairo departure, international destinations)
- Passport validation and uniqueness checks
- Multi-browser compatibility
- Multi-language support

**Key Features Tested:**
- Date range validations
- Geographic and route restrictions
- Passport number validation
- Browser compatibility
- Internationalization

## 🎯 Test Case Categories

### Positive Test Cases
- Happy path scenarios with valid data
- Boundary value testing
- Successful user workflows
- Feature functionality verification

### Negative Test Cases
- Invalid input handling
- Error message validation
- Security boundary testing
- Exception handling verification

## 📋 Test Execution Guidelines

### Pre-Test Setup
1. Ensure all required test environments are available
2. Prepare test data as specified in each test case file
3. Verify system configurations and dependencies
4. Clear browser cache and reset test databases

### Test Data Requirements
Each test case file includes specific test data requirements:
- Valid and invalid input examples
- User account credentials
- Product/service data
- Configuration parameters

### Post-Test Activities
1. Document test results and defects
2. Clean up test data
3. Reset system states
4. Generate test execution reports

## 🔧 Testing Tools

### Test Types Covered
- Functional Testing
- UI/UX Testing
- Validation Testing
- Error Handling Testing
- Cross-browser Testing
- Internationalization Testing

## 📈 Test Metrics

### Coverage Areas
- User Authentication & Authorization
- Payment Processing
- Form Validation
- Cart Management
- Subscription Services
- Booking Systems
- Contact & Communication

### Priority Levels
- **High**: Critical business functionality
- **Medium**: Important features with moderate impact
- **Low**: Nice-to-have features
