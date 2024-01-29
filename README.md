
# Lecture Practice - Logical Operators

## Introduction

Logical operators are utilized alongside comparison operators to address questions that involve multiple conditions with both affirmative and negative requirements.

**Logical Operators Table:**

| Operator | Description | Example | Result |
| ---- | ---- | ---- | ---- |
| `&&` | Logical AND | `true && true` | `true` |
| \|\| | Logical Or | `true \|\| false` | `true` |
| `!` | Logical NOT | `!true` | `false` |

**Comparison Operators Table:**

| Operator | Description | Example | Result |
|----------|-------------|---------|--------|
| `==`     | Equal       | `5 == 5` | `true` |
| `!=`     | Not Equal   | `5 != 3` | `true` |
| `<`      | Less Than   | `3 < 5` | `true` |
| `>`      | Greater Than| `5 > 3` | `true` |
| `<=`     | Less Than or Equal | `3 <= 3` | `true` |
| `>=`     | Greater Than or Equal | `5 >= 5` | `true` |
## Explanation

### Below is the logic that's used to deconstruct a question into individual variables and then display the result.

**Question: Can a user enter a club if they are at least 18 years old (isOver18) and have a valid membership (hasMembership)?**

Now, let's break it down step by step:

1. **Identify Conditions:**
   - We need to determine if a user can enter a club based on two conditions:
     - Condition 1: Is the user at least 18 years old? (represented as `isOver18`)
     - Condition 2: Does the user have a valid membership? (represented as `hasMembership`)

2. **Declare Variables:**
   - Create boolean variables to represent each of the identified conditions:

```csharp
bool isOver18;
bool hasMembership;
```

3. **Perform Comparisons:**
   - For the conditions, perform the necessary comparisons:

```csharp
// Assume you have functions or inputs to determine these values.
bool isOver18 = true; // Example: Assume the user is 18 years old or older.
bool hasMembership = true; // Example: Assume the user has a valid membership.
```

4. **Combine Conditions:**
   - Combine the conditions using logical operators to answer the main question:

```csharp
bool canEnterClub = isOver18 && hasMembership;
```

5. **Display the Result:**
   - Finally, display the result to answer the question based on the value of `canEnterClub`:

```csharp
if (canEnterClub)
{
    Console.WriteLine("The user can enter the club.");
}
else
{
    Console.WriteLine("The user cannot enter the club.");
}
```

## Expected Results with Testing

| isOver18 | hasMembership | canEnterClub | Output                                |
|----------|---------------|--------------|---------------------------------------|
| true     | true          | true         | The user can enter the club.         |
| true     | false         | false        | The user cannot enter the club.      |
| false    | true          | false        | The user cannot enter the club.      |
| false    | false         | false        | The user cannot enter the club.      |

---
# Assignment

- Create a new project called LP_LogicalOperations_YourName
- Comment your name at the top of the assignment
- Copy and paste the following questions from below, adding the required code and testing along the way.
- Submit your project on Canvas with a GitHub repo.

## Questions 1 - 7

1. **Question 1: Checking if a Number is Even or Positive (Easier)**
### ***Question: Is a given number even AND positive?***

   Given an integer variable `num`, create bool variables `isEven` and `isPositive` to check if `num` is even and positive, respectively. Then, create a bool variable `isEvenAndPositive` that combines these conditions using a logical operator. Display the result.

   > Tip: You can compare numbers with >, <, >=, \<=, ==, and !=  
   > Check the Required Logic table below for assistance

   **Comparison Operators Table:**

| Operator | Description | Example | Result |
|----------|-------------|---------|--------|
| `==`     | Equal       | `5 == 5` | `true` |
| `!=`     | Not Equal   | `5 != 3` | `true` |
| `<`      | Less Than   | `3 < 5` | `true` |
| `>`      | Greater Than| `5 > 3` | `true` |
| `<=`     | Less Than or Equal | `3 <= 3` | `true` |
| `>=`     | Greater Than or Equal | `5 >= 5` | `true` |

### Copy and paste this code into the `main` in your `Program.cs`

   ```csharp
   int num = 6;
   // Requires Comparison Operator: Checking if num is even
   bool isEven;
   // Requires Comparison Operator: Checking if num is positive
   bool isPositive;
   // Requires Logical Operator: Combining isEven and isPositive
   bool isEvenAndPositive;
   Console.WriteLine($"Is 'num' even and positive? {isEvenAndPositive}");
   ```

### Required Logic
| Operation | Explanation | Example |  |
| ---- | ---- | ---- | ---- |
| Check for Even | Use the modulus operator `%` to check if the remainder when dividing the number by 2 is equal to 0. If it's equal to 0, the number is even. | `bool isEven = (num % 2 == 0);` |  |
| Check for Positive | Use the greater than `>` operator to check if the number is greater than 0. If it's greater than 0, the number is positive. | `bool isPositive = (num > 0);` |  |

## Run Code

Test with these 3 numbers and compare your results

| `num` | `isEven` | `isPositive` | `isEvenAndPositive` | Output                                |
|-------|----------|--------------|----------------------|---------------------------------------|
| 6     | true     | true         | true                 | Is 'num' even and positive? True      |
| 7     | false    | true         | false                | Is 'num' even and positive? False     |
| -8    | true     | false        | false                | Is 'num' even and positive? False     |

---

2. **Question 2: Checking User Role (Easier)**
### ***Question: Is the user an "admin" OR a "moderator"***

   You have a string variable `input` representing a user's role. Create bool variables `isAdmin` and `isModerator` to check if the user is an "admin" or a "moderator," respectively. Then, create a bool variable `isAuthorized` that checks if the user is authorized based on these conditions using a logical operator. Display the result.

   > Tip: Here you are comparing strings, use ==

   ### Copy and paste this code into the `main` in your `Program.cs`
   ```csharp
   string input = "moderator";
   // Requires Comparison Operator: Checking if input is "admin"
   bool isAdmin;
   // Requires Comparison Operator: Checking if input is "moderator"
   bool isModerator;
   // Requires Logical Operator: Combining isAdmin and isModerator
   bool isAuthorized;
   Console.WriteLine($"Is the user authorized? {isAuthorized}");
   ```


## Run the code and compare results

| `input`   | `isAdmin` | `isModerator` | `isAuthorized` | Output                   |
|-----------|-----------|---------------|----------------|--------------------------|
| "admin"   | true      | false         | true           | Is the user authorized? True   |
| "moderator"| false     | true          | true           | Is the user authorized? True   |
| "user"    | false     | false         | false          | Is the user authorized? False  |

---

3. **Question 3: Checking Age Eligibility (Easy)**

### ***Question: Is the voter 18 or older AND 100 or younger"***

**Question: Checking Voter Eligibility (Revised with Logical Operator)**
Given an integer variable `age`, create a bool variable `isEligibleToVote` that checks if a person is eligible to vote by using a logical operator to ensure that the age is within a reasonable voting age range (between 18 and 100). Display the result.

> Tip: Using \<= checks if a value is lesser than OR equal to. The same applies to >= for greater than or equal to.  
> 10 > 10 - False  
> 10 >= 10 - True

### Copy and paste this code into the `main` in your `Program.cs`

```csharp
int age = 21;

// Requires Comparison Operator: Checking if age is greater than or equal to 18
bool isAgeAtLeast18;

// Requires Comparison Operator: Checking if age is less than or equal to 100
bool isAgeAtMost100;

// Requires Logical Operator: Combining isAgeAtLeast18 and isAgeAtMost100 using logical AND
bool isEligibleToVote;

Console.WriteLine($"Is the person eligible to vote? {isEligibleToVote}");

```


## Run the code and compare

| `age` | `isAgeAtLeast18` | `isAgeAtMost100` | `isEligibleToVote` | Output                                 |
|-------|-------------------|-------------------|--------------------|----------------------------------------|
| 21    | true              | true              | true               | Is the person eligible to vote? True   |
| 17    | false             | true              | false              | Is the person eligible to vote? False  |
| 101   | true              | false             | false              | Is the person eligible to vote? False  |

---

4. **Question 4: Checking Online Status and Login using Logical Operator (Medium)**

### ***Question: Is the user online AND logged in***

   Given two boolean variables `isOnline` and `isLoggedIn`, create a bool variable `canAccess` that checks if the user can access a system based on both `isOnline` and `isLoggedIn` using a logical operator. Display the result.

   ### Copy and paste this code into the `main` in your `Program.cs`

   ```csharp
   bool isOnline = true;
   bool isLoggedIn = true;
   // Requires Logical Operator: Combining isOnline and isLoggedIn
   bool canAccess;
   Console.WriteLine($"Can the user access? {canAccess}");
   ```

5. **Question 5: Checking Player's High Score using Logical Operator (Medium)**

### ***Question: Is players score equal to or greater than 1000 AND less than or equal to 5000"***

   Create bool variables `isHighScore` and `isLowScore` to check if `playerScore` is both greater than or equal to 1000 and less than or equal to 5000, respectively. Then, create a bool variable `isHighOrLowScore` that combines these conditions using a logical operator. Display the result.

   ### Copy and paste this code into the `main` in your `Program.cs`

   ```csharp
   int playerScore = 1200;
   // Requires Comparison Operator: Checking if playerScore is greater than or equal to 1000
   bool isHighScore;
   // Requires Comparison Operator: Checking if playerScore is less than or equal to 5000
   bool isLowScore;
   // Requires Logical Operator: Combining isHighScore and isLowScore
   bool isHighOrLowScore;
   Console.WriteLine($"Is the player's score a high or low score? {isHighOrLowScore}");
   ```


## Run code and compare

| `playerScore` | `isHighScore` | `isLowScore` | `isHighOrLowScore` | Output                                       |
|---------------|---------------|--------------|--------------------|----------------------------------------------|
| 1200          | true          | true         | true               | Is the player's score a high or low score? True |
| 500           | true          | true         | true               | Is the player's score a high or low score? True |
| 6000          | true          | false        | false              | Is the player's score a high or low score? False |
| 8000          | true          | false        | false              | Is the player's score a high or low score? False |

---

6. **Question 6: Subscription Access Control using Logical Operator (Medium)**
### ***Question: Has the user paid OR the trial has NOT expired"***
   
   Given bool variables `hasPaid` and `isTrialExpired`, create bool variables `canAccessWithPayment` and `canAccessWithTrial` to check if the user can access content based on having paid or not having the trial expired. Then, create a bool variable `canAccessContent` that combines these conditions using a logical operator. Display the result.

   > Tip: You can invert any boolean with a !.  
   > bool isRaining = true;  
   > bool isNOTRaining = !isRaining; Flips true to false  


   ### Copy and paste this code into the `main` in your `Program.cs`

   ```csharp
   bool hasPaid = false;
   bool isTrialExpired = false;
   // Requires Logical Operator: Combining hasPaid and isTrialExpired
   bool canAccessWithPayment;
   // Requires Logical Operator: Negating isTrialExpired
   bool canAccessWithTrial;
   // Requires Logical Operator: Combining canAccessWithPayment and canAccessWithTrial
   bool canAccessContent;
   Console.WriteLine($"Can the user access content? {canAccessContent}");
   ```


### Run Code and Compare

Certainly! Here's a table of possible results for the given code with different values for the `hasPaid` and `isTrialExpired` boolean variables:

| `hasPaid` | `isTrialExpired` | `canAccessWithPayment` | `canAccessWithTrial` | `canAccessContent` | Output                                 |
|-----------|-------------------|-------------------------|-----------------------|--------------------|----------------------------------------|
| false     | false             | false                   | true                  | true               | Can the user access content? True      |
| true      | false             | true                    | true                  | true               | Can the user access content? True      |
| false     | true              | false                   | false                 | false              | Can the user access content? False     |
| true      | true              | true                    | false                 | true               | Can the user access content? True      |

In this table, `hasPaid` and `isTrialExpired` represent different combinations of the boolean variables. The `canAccessWithPayment` and `canAccessWithTrial` variables are calculated based on the given conditions, and `canAccessContent` is computed by combining the results of `canAccessWithPayment` and `canAccessWithTrial` using the logical OR operator (`||`). The output is displayed as "Can the user access content? {canAccessContent}" for each combination of `hasPaid` and `isTrialExpired`.


---

7. **Question 7: Complex Access Control System with Multiple Conditions**

***Question 7: ***
Imagine you're tasked with developing a sophisticated access control system for a highly secure facility. This system involves multiple levels of access control, and each level has specific requirements:

- Level 1: Users must have a valid access card to enter the facility.
- Level 2: To proceed further, users must also provide a biometric scan.
- Level 3: Finally, access is granted only if the user has a security clearance level of 5 or higher.

**Starting Variables Explanation:**

- `hasAccessCard`: This variable represents whether a user possesses a valid access card (`true` if they have one, `false` if they don't).
- `hasBiometricScan`: Indicates whether the user has successfully provided a biometric scan (`true` if they have, `false` if they haven't).
- `securityClearanceLevel`: This integer variable stores the security clearance level of the user, with a placeholder value of `4`. In practice, you'd replace this value with the actual security clearance level of the user.

> Tip: We can use Parenthese for order of operations when working with booleans.

`Code Examples, Don't Copy and Paste`
```csharp
    // Example 1: Using parentheses to control the order of operations
    bool a = true;
    bool b = false;
    bool c = true;

    bool result = (a && b) || c;
    // Here, the '&&' operation is evaluated before '||' because of parentheses.
    // (true && false) is false, so the result is true (true || true).
    Console.WriteLine(result);  // Output: True
```

Here's the code snippet that implements this complex access control system:

### Copy and paste this code into the `main` in your `Program.cs`

```csharp
bool hasAccessCard = true;
bool hasBiometricScan = true;
int securityClearanceLevel = 4; // Replace with an actual security clearance level.

// Requires Comparison Operator: Checking if the user has a valid access card
bool canEnter;

// Requires Logical Operator: Combining canEnter and checking if the user has a biometric scan
bool canProceedToLevel2;

// Requires Logical Operator: Combining canProceedToLevel2 and checking if the security clearance level is 5 or higher
bool canProceedToLevel3;

Console.WriteLine("Level 1 - Can Enter: " + canEnter);
Console.WriteLine("Level 2 - Can Proceed (Biometric Scan): " + canProceedToLevel2);
Console.WriteLine("Level 3 - Can Proceed (Security Clearance): " + canProceedToLevel3);
```

### Run Code and Compare

Assuming `true` represents having the respective condition, and `false` represents not having it.

| `hasAccessCard` | `hasBiometricScan` | `securityClearanceLevel` | `canEnter` | `canProceedToLevel2` | `canProceedToLevel3` |
|-----------------|---------------------|--------------------------|------------|----------------------|----------------------|
| true            | true                | (e.g., 4)                | true       | true                 | false                |
| true            | true                | (e.g., 5)                | true       | true                 | true                 |
| true            | false               | (e.g., 4)                | true       | false                | false                |
| false           | true                | (e.g., 4)                | false      | false                | false                |
| false           | false               | (e.g., 4)                | false      | false                | false                |

---

# Rubric

| Criteria                               | Description                                 | Points |
|----------------------------------------|---------------------------------------------|--------|
| **Correctness**                        | Evaluate the accuracy of implemented logic and conditions. Ensure the code provides accurate results according to the specified conditions and requirements. | 30     |
| **Code Structure and Organization**    | Assess the structure and organization of the code, including variable naming, logical flow, and proper indentation. | 15     |
| **Testing and Output**                 | Evaluate the adequacy of testing with different inputs and the extent to which the output matches the expected results for various scenarios. | 15     |
| **Comments and Documentation**         | Check for the presence of appropriate comments and documentation that explain the purpose of the code and how it works. | 10     |
| **Project Naming and Submission**      | Verify that the project is named correctly as per the assignment instructions and that the assignment has been properly submitted on the specified platform (Canvas or GitHub). | 5      |
| **Answering Question 1**               | Assess the accuracy and completeness of the answer to Question 1, which involves checking if a given number is even and positive. | 5      |
| **Answering Question 2**               | Evaluate the accuracy and completeness of the answer to Question 2, which involves checking the user's role for "admin" or "moderator." | 5      |
| **Answering Question 3**               | Assess the accuracy and completeness of the answer to Question 3, which involves checking voter eligibility based on age. | 5      |
| **Answering Question 4**               | Evaluate the accuracy and completeness of the answer to Question 4, which involves checking the user's online status and login. | 5      |
| **Answering Question 5**               | Assess the accuracy and completeness of the answer to Question 5, which involves checking the player's high score. | 5      |
| **Answering Question 6**               | Evaluate the accuracy and completeness of the answer to Question 6, which involves checking subscription access control. | 5      |
| **Answering Question 7**               | Assess the accuracy and completeness of the answer to Question 7, which involves implementing a complex access control system with multiple conditions. | 10     |
| **Total Points**                       |                                           | 100    |
