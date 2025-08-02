# Aviation Portal Test Cases

## Description
Aviation portal offering flight booking discounts with specific conditions and requirements for eligibility.

## Business Rules
- **Discount**: 20% discount on flight bookings
- **Booking Period**: December 15-18, 2018
- **Flight Period**: December 29, 2018 - January 3, 2019
- **Departure Requirement**: Must start from Cairo
- **Destination Requirement**: Must be international (outside Egypt)
- **Passport Requirement**: Valid and unique passport number
- **Usage Limit**: One discount per passport number

---

## Test Cases

### Positive Test Cases

| Test Case ID | Test Case Title | Pre-condition | Test Case Steps | Priority | Expected Results |
|--------------|-----------------|---------------|-----------------|----------|------------------|
| TC_001 | Validate discount applied when all conditions are met | - Portal works in Chrome browser<br>- Valid and unique passport number | 1. Navigate to Aviation Portal<br>2. Select departure city: Cairo<br>3. Select destination: Dubai<br>4. Select flight date: 30/12/2018<br>5. Submit booking on 16/12/2018<br>6. Enter unique passport number<br>7. Complete booking process | High | - Booking completed successfully<br>- 20% discount applied on total flight amount |
| TC_002 | Validate discount applied on booking period start date | - Portal works in Internet Explorer<br>- Valid and unique passport number | 1. Navigate to Aviation Portal<br>2. Select departure city: Cairo<br>3. Select destination: London<br>4. Select flight date: 2/1/2019<br>5. Submit booking on 15/12/2018<br>6. Enter unique passport number<br>7. Complete booking process | High | - Booking completed successfully<br>- 20% discount applied on total flight amount |
| TC_003 | Validate discount applied on booking period end date | - Portal works in Firefox browser<br>- Valid and unique passport number | 1. Navigate to Aviation Portal<br>2. Select departure city: Cairo<br>3. Select destination: New York<br>4. Select flight date: 1/1/2019<br>5. Submit booking on 18/12/2018<br>6. Enter unique passport number<br>7. Complete booking process | High | - Booking completed successfully<br>- 20% discount applied on total flight amount |
| TC_004 | Validate discount applied on flight period start date | - Portal works in Chrome browser<br>- Valid and unique passport number | 1. Navigate to Aviation Portal<br>2. Select departure city: Cairo<br>3. Select destination: Riyadh<br>4. Select flight date: 29/12/2018<br>5. Submit booking on 17/12/2018<br>6. Enter unique passport number<br>7. Complete booking process | High | - Booking completed successfully<br>- 20% discount applied on total flight amount |
| TC_005 | Validate discount applied on flight period end date | - Portal works in Firefox browser<br>- Valid and unique passport number | 1. Navigate to Aviation Portal<br>2. Select departure city: Cairo<br>3. Select destination: Paris<br>4. Select flight date: 3/1/2019<br>5. Submit booking on 16/12/2018<br>6. Enter unique passport number<br>7. Complete booking process | High | - Booking completed successfully<br>- 20% discount applied on total flight amount |
| TC_006 | Validate multiple languages support in the portal | - Portal works in Chrome browser<br>- Valid and unique passport number | 1. Navigate to Aviation Portal<br>2. Select departure city: Cairo<br>3. Select destination: Dubai<br>4. Select flight date: 30/12/2018<br>5. Test booking in each language:<br>   - French, German, Spanish, Italian, Japanese<br>6. Verify discount calculations<br>7. Verify translations accuracy<br>8. Check special characters display<br>9. Complete booking process | Medium | - Booking completed with 20% discount<br>- Discount functionality works in all languages<br>- Translations display correctly<br>- No character encoding issues |

### Negative Test Cases

| Test Case ID | Test Case Title | Pre-condition | Test Case Steps | Priority | Expected Results |
|--------------|-----------------|---------------|-----------------|----------|------------------|
| TC_007 | Validate invalid passport number handling | - Portal works in Internet Explorer<br>- Invalid passport number available | 1. Navigate to Aviation Portal<br>2. Select departure city: Cairo<br>3. Select destination: Berlin<br>4. Select flight date: 30/12/2018<br>5. Submit booking on 17/12/2018<br>6. Enter invalid passport number<br>7. Complete booking process | High | - Discount should not apply<br>- Error message: "Passport number invalid" |
| TC_008 | Validate previously used passport number rejection | - Portal works in Chrome browser<br>- Passport number used before for this offer | 1. Navigate to Aviation Portal<br>2. Select departure city: Cairo<br>3. Select destination: Tokyo<br>4. Select flight date: 1/1/2019<br>5. Submit booking on 15/12/2018<br>6. Enter previously used passport number<br>7. Complete booking process | High | - Discount should not apply<br>- Error message: "This passport number took this offer before" |
| TC_009 | Validate no discount for domestic flights from Cairo | - Portal works in Firefox browser<br>- Valid and unique passport number | 1. Navigate to Aviation Portal<br>2. Select departure city: Cairo<br>3. Select destination: Alexandria<br>4. Select flight date: 2/1/2019<br>5. Submit booking on 17/12/2018<br>6. Enter unique passport number<br>7. Complete booking process | High | - Booking completed without discount<br>- No discount applied |
| TC_010 | Validate no discount when departure is not from Cairo | - Portal works in Internet Explorer<br>- Valid and unique passport number | 1. Navigate to Aviation Portal<br>2. Select departure city: Rome<br>3. Select destination: Cairo<br>4. Select flight date: 3/1/2019<br>5. Submit booking on 16/12/2018<br>6. Enter unique passport number<br>7. Complete booking process | High | - Booking completed without discount<br>- No discount applied |
| TC_011 | Validate invalid route (Cairo to Cairo) | - Portal works in Chrome browser<br>- Valid and unique passport number | 1. Navigate to Aviation Portal<br>2. Select departure city: Cairo<br>3. Select destination: Cairo<br>4. Select flight date: 1/1/2019<br>5. Submit booking on 18/12/2018<br>6. Enter unique passport number<br>7. Complete booking process | Medium | - Booking should not complete<br>- Error message: "Invalid departure city or destination" |
| TC_012 | Validate no discount for booking before valid period | - Portal works in Firefox browser<br>- Valid and unique passport number | 1. Navigate to Aviation Portal<br>2. Select departure city: Cairo<br>3. Select destination: Dubai<br>4. Select flight date: 30/12/2018<br>5. Submit booking on 14/12/2018<br>6. Enter unique passport number<br>7. Complete booking process | High | - Booking completed without discount<br>- No discount applied |
| TC_013 | Validate no discount for booking after valid period | - Portal works in Internet Explorer<br>- Valid and unique passport number | 1. Navigate to Aviation Portal<br>2. Select departure city: Cairo<br>3. Select destination: Rome<br>4. Select flight date: 29/12/2018<br>5. Submit booking on 19/12/2018<br>6. Enter unique passport number<br>7. Complete booking process | High | - Booking completed without discount<br>- No discount applied |
| TC_014 | Validate no discount for flight before valid period | - Portal works in Firefox browser<br>- Valid and unique passport number | 1. Navigate to Aviation Portal<br>2. Select departure city: Cairo<br>3. Select destination: London<br>4. Select flight date: 28/12/2018<br>5. Submit booking on 17/12/2018<br>6. Enter unique passport number<br>7. Complete booking process | High | - Booking completed without discount<br>- No discount applied |
| TC_015 | Validate no discount for flight after valid period | - Portal works in Chrome browser<br>- Valid and unique passport number | 1. Navigate to Aviation Portal<br>2. Select departure city: Cairo<br>3. Select destination: Madrid<br>4. Select flight date: 4/1/2019<br>5. Submit booking on 16/12/2018<br>6. Enter unique passport number<br>7. Complete booking process | High | - Booking completed without discount<br>- No discount applied |


## Test Data Requirements

### Valid Passport Numbers
- **Format Examples**:
  - US: 123456789
  - UK: 123456789
  - German: C01X00T47
  - Egyptian: A12345678

### Invalid Passport Numbers
- **Invalid Formats**:
  - Too short: 12345
  - Too long: 1234567890123
  - Invalid characters: 12345@#$%
  - Empty field: ""

### City Data
- **Valid Departure Cities**: Cairo
- **Valid International Destinations**: 
  - Dubai, London, New York, Paris, Tokyo, Berlin, Rome, Madrid, Riyadh
- **Valid Domestic Destinations**: 
  - Alexandria, Aswan, Luxor, Sharm El Sheikh

### Date Ranges
- **Valid Booking Dates**: December 15-18, 2018
- **Valid Flight Dates**: December 29, 2018 - January 3, 2019
- **Invalid Dates**: Any dates outside specified ranges


## Pre-test Checklist
1. **Data Setup**:
   - Flight schedules loaded for test dates
   - City and airport data configured
   - Discount rules properly configured
   - Test passport numbers prepared

2. **System Setup**:
   - All browsers installed and updated
   - Test accounts created
   - Payment gateway in test mode
   - Logging and monitoring enabled

3. **Environment Verification**:
   - Portal accessibility confirmed
   - Database connectivity verified
   - Email notifications working
   - Backup and recovery procedures ready

---

## Post-test Activities
1. **Results Documentation**:
   - Test execution results recorded
   - Defects logged with severity levels
   - Performance metrics documented
   - Security findings reported

2. **Data Cleanup**:
   - Test bookings removed from database
   - Used passport numbers reset
   - Test user sessions cleared
   - Temporary files deleted

3. **Reporting**:
   - Test summary report generated
   - Coverage analysis completed
   - Recommendations documented
   - Sign-off obtained from stakeholders

---

## Success Criteria
- **Functional**: All high-priority test cases pass
- **Security**: No critical security vulnerabilities
- **Performance**: Response times under 3 seconds
- **Compatibility**: Works across all specified browsers
- **Usability**: User workflows complete without confusion
- **Data Integrity**: All business rules enforced correctly