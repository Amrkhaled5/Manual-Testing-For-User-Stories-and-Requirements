# Quiz Game Feature Test Cases

## Description
Quiz game where users with active subscription can play and get rewards upon successful completion.

## User Experience Requirements
- Quiz game consisting of 5 questions
- Each question has 4 answers that may be either text or image-based
- User must have active subscription to access the game
- If user answers all 5 questions correctly, they receive a reward
- If user answers one question incorrectly, they lose and can play again
- Game provides feedback on each question's correct answer
- System tracks user progress through the game

---

## Test Cases

### Positive Test Cases

| Test Case ID | Test Case Title | Pre-condition | Test Case Steps | Priority | Expected Results |
|--------------|-----------------|---------------|-----------------|----------|------------------|
| TC_001 | Validate user with subscription takes quiz game and answers all questions correctly to receive reward | - Working software<br>- Valid user account with active subscription | 1. Open the app<br>2. Login with subscribed user<br>3. Navigate to quiz game<br>4. Start quiz game<br>5. Answer all 5 questions correctly<br>6. Click Submit | High | - Game ends successfully<br>- User receives reward<br>- Reward added to user account |
| TC_002 | Validate system handles mixed questions with text and images in answer options | - Working software<br>- Valid user account with active subscription<br>- Quiz has answers with both text and images | 1. Open the app<br>2. Login with subscribed user<br>3. Navigate to quiz game<br>4. Start quiz game<br>5. Interact with both text and image answers<br>6. Answer all questions<br>7. Click Submit | Medium | - Both text and image answers display correctly<br>- User can select text and image answers by clicking<br>- Game functions properly with mixed content |
| TC_003 | Validate user with subscription takes quiz, answers one question wrong, and can play again | - Working software<br>- Valid user account with active subscription | 1. Open the app<br>2. Login with subscribed user<br>3. Navigate to quiz game<br>4. Start quiz game<br>5. Answer 4 questions correctly and 1 wrong<br>6. Click Submit<br>7. Click "Play Again" | High | - Game ends with failure<br>- User sees correct answers feedback<br>- "Play Again" option appears<br>- User can restart the game |
| TC_004 | Validate user can track progress through the game | - Working software<br>- Valid user account with active subscription | 1. Open the app<br>2. Login with subscribed user<br>3. Navigate to quiz game<br>4. Start quiz game<br>5. Answer 3 questions<br>6. Observe progress indicator | Medium | - User can see current question number<br>- Progress shows "Question X of 5"<br>- Progress updates correctly as user advances |
| TC_005 | Validate user can get reward after initially losing then winning | - Working software<br>- Valid user account with active subscription | 1. Open the app<br>2. Login with subscribed user<br>3. Navigate to quiz game<br>4. Start quiz game<br>5. Answer 4 correctly, 1 wrong<br>6. Click Submit<br>7. Click "Play Again"<br>8. Answer all questions correctly<br>9. Click Submit | Medium | - User can play again after first failure<br>- Feedback appears after first attempt<br>- After second successful attempt, game ends<br>- User receives reward and it's added to account |

### Negative Test Cases

| Test Case ID | Test Case Title | Pre-condition | Test Case Steps | Priority | Expected Results |
|--------------|-----------------|---------------|-----------------|----------|------------------|
| TC_006 | Validate user login with expired or inactive subscription | - Working software<br>- Valid user account with expired/inactive subscription | 1. Open the app<br>2. Login with user having expired subscription<br>3. Navigate to quiz game<br>4. Attempt to start quiz game | High | - User cannot start quiz game<br>- Error message: "Active subscription required"<br>- User redirected to subscription page |
| TC_007 | Validate user access quiz game without login | - Working software<br>- No user logged in | 1. Open the app<br>2. Navigate to quiz game<br>3. Attempt to start quiz game | High | - User cannot start quiz game<br>- Error message: "Need to login"<br>- User redirected to login page |
