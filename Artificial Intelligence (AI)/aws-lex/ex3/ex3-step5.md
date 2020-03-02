# Step 5 (Optional): Capturing and Validating Alphanumeric Identifiers

In this section, you can use `AMAZON.AlphaNumeric` slot type in Amazon Lex to capture such inputs in your bot. This slot type can capture combinations of letters and numbers. You can extend this slot type by applying a validation check to create a custom slot type. You can apply these validation checks by specifying a regular expression (regex) on the `AMAZON.AlphaNumeric` slot type. This post demonstrates how to use the `AMAZON.AlphaNumeric` slot type to capture alphanumeric information and restrict such input to a specific pattern.

## Create New Slot Type

You can create the built-in slot type `AMAZON.AlphaNumeric`. Such a design helps capture alphanumeric information but doesn’t validate it. To validate, use a regular expression. Create a new slot type FlightNo by extending `AMAZON.AlphaNumeric`. The flight number has a fixed format of six characters: [letter] [letter][number][number][number][number]. For example, HK2020 is a flight number.

1. In the Amazon Lex console, choose the **BookTrip** bot. 

1. On the **Editor** tab, next to **Slot types**, choose the plus sign.

1. Choose **Extend slot type**.
![](../images/ex3-step5-01.png)

l. For **Slot type name**, enter `FlightNo`.

1. For **Description**, enter a description (`Flight Number`) of your slot type.

1. For **Regular expression**, restrict the slot type to the six-character fixed format as specified previously by entering the expression `[A-Z]{2}[0-9]{4}`.

1. Choose **Save slot type**.
![](../images/ex3-step5-02.png)


## Add New Slot Type to Your Bot
You can now use the `FlightNo` slot type to design the `BookHotel` intent for your bot and make sure that the user input contains a valid flight number.

To add the `FlightNo` slot type to the `BookHotel` intent, complete the following steps:

1. In the Amazon Lex console, choose the **BookTrip** bot. 
1. On the **Editor** tab, under **Intents**, choose `BookHotel`.
1. Under **Slots**, add a new slot `ArrivalFlightNo` with Slot type `FlightNo` with an appropriate prompt (`Please provide us your arrival flight number for free airport delivery`).
1. Design the rest of the bot as per your use-case.
1. Choose **Save Intent**, **Build**, and **Publish**.

Your bot is now ready to use. You can test it by providing a flight number such as ABCDE that does not match the pattern specified by the regular expression.