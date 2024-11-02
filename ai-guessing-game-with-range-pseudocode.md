## Pseudocode for Guessing Game 2.0

### Notes About The Pseudocode:
- **BEGIN/END**: Marks the start and end of the script.
- **SET**: Used to initialize variables.
- **PRINT**: Displays messages to the user; use either **concatenation** or **f-strings** in this script.
- **GET**: Represents user input.
- **FOR Loop**: Used for the user's guesses; loops (*iterates*) a certain number of times before the loop exits.
- **IF-ELSE Statements**: Checks conditions for the guesses and provides feedback based on the user's guesses.

```
BEGIN GuessingGame

    // Define a list of numbers from 1 to 10
    SET numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

    // Randomly select a secret number from the list
    SET secret_number = random choice from numbers

    // Set the number of attempts allowed
    SET attempts = 3
    PRINT "Welcome to the Guessing Game!"
    PRINT "I'm thinking of a number between 1 and 10. You have 3 attempts to guess it."

    // Loop through each attempt
    FOR attempt FROM 1 TO attempts DO

        // Prompt user for their guess
        PRINT "Attempt " + attempt + ": Enter your guess:"
        GET user input as guess

        // Check if the guess is out of range
        IF guess < 1 OR guess > 10 THEN
            PRINT "Please guess a number between 1 and 10."
        
        // Check if the guess is correct
        ELSE IF guess == secret_number THEN
            PRINT "Congratulations! You guessed the number!"
            BREAK // Exit the loop

        // If the guess is incorrect
        ELSE
            PRINT "Wrong guess. Try again!"

    // After attempts, reveal the secret number if not guessed
    IF guess != secret_number THEN
        PRINT "Sorry! The correct number was " + secret_number + ". Better luck next time!"

END GuessingGame
```



