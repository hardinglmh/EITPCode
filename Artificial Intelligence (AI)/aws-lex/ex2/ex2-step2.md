# Step 2: Create a Bot

In this step, you create a bot to handle pizza orders.

## Create the Bot

Create the `PizzaOrderingBot` bot with the minimum information needed\. You add an intent, an action that the user wants to perform, for the bot later\.

**To create the bot**

1. Sign in to the AWS Management Console and open the Amazon Lex console at [https://console\.aws\.amazon\.com/lex/](https://console.aws.amazon.com/lex/)\.

1. Create a bot\.

   1. Choose **Bots**, and then choose **Create**\. 

   1. On the **Create your bot** page, choose **Custom bot** and provide the following information:
      + **App name**: PizzaOrderingBot 
      + **Output voice**: Salli 
      + **Session timeout**: 5 minutes
      + **COPPA**: No

   1. Choose **Create**\. 

      The console sends Amazon Lex a request to create a new bot\. Amazon Lex sets the bot version to `$LATEST`\. After creating the bot, Amazon Lex shows the bot **Editor** tab:  
../images/gs1-20.png)
      + The bot version, **Latest**, appears next to the bot name in the console\. New Amazon Lex resources have `$LATEST` as the version\.
      + Because you haven't created any intents or slots types, none are listed\. 
      + **Build** and **Publish** are bot\-level activities\. After you configure the entire bot, you'll learn more about these activities\.

      
## Create an Intent

Now, create the `OrderPizza` intent , an action that the user wants to perform, with the minimum information needed\. You add slot types for the intent and then configure the intent later\.

**To create an intent**

1. In the Amazon Lex console, choose the plus sign \(\+\) next to **Intents**, and then choose **Create new intent**\.

1. In the **Create intent** dialog box, type the name of the intent \(`OrderPizza`\), and then choose **Add**\.

The console sends a request to Amazon Lex to create the `OrderPizza` intent\. In this example you create slots for the intent after you create slot types\.


## Create Slot Types

Create the slot types, or parameter values, that the `OrderPizza` intent uses\.

**To create slot types**

1. <a name="slotTypeStart"></a>In the left menu, choose the plus sign \(\+\) next to **Slot types**\.

1. In the **Add slot type** dialog box, add the following: 
   + **Slot type name** – Crusts
   + **Description** – Available crusts
   + Choose **Restrict to Slot values and Synonyms**
   + **Value** – Type **thick**\. Press tab and in the **Synonym** field type **stuffed**\. Choose the plus sign \(\+\)\. Type **thin** and then choose the plus sign \(\+\) again\.

   The dialog should look like this:  
![\[The edit slot type dialog box.\]](../images/gs1-25a.png)

1. Choose **Add slot to intent**\.

1. <a name="slotTypeFinish"></a>On the **Intent** page, choose **Required**\. Change the name of the slot from **slotOne** to **crust**\. Change the prompt to **What kind of crust would you like?**

1. Repeat [Step 1](#slotTypeStart) through [Step 4](#slotTypeFinish) using the values in the following table:    
![\[The intent editor.\]](../images/gs1-30.png)


## Configure the Intent

Configure the `OrderPizza` intent to fulfill a user's request to order a pizza\.

**To configure an intent**
+ On the **OrderPizza** configuration page, configure the intent as follows:
  + **Sample utterances** – Type the following strings\. The curly braces \{\} enclose slot names\.
    + I want to order pizza please 
    + I want to order a pizza
    + I want to order a \{pizzaKind\} pizza
    + I want to order a \{size\} \{pizzaKind\} pizza 
    + I want a \{size\} \{crust\} crust \{pizzaKind\} pizza
    + Can I get a pizza please
    + Can I get a \{pizzaKind\} pizza
    + Can I get a \{size\} \{pizzaKind\} pizza
  + **Lambda initialization and validation** – Leave the default setting\.
  + **Confirmation prompt** – Leave the default setting\.
  + **Fulfillment** – Perform the following tasks:
    + Choose **AWS Lambda function**\.
    + Choose **PizzaOrderProcessor**\. 
    + If the **Add permission to Lambda function** dialog box is shown, choose **OK** to give the `OrderPizza` intent permission to call the `PizzaOrderProcessor` Lambda function\.
    +  Leave **None** selected\.

  The intent should look like the following:  
![\[The intent editor.\]](../images/gs1-70c.png)


## Configure the Bot

Configure error handling for the `PizzaOrderingBot` bot\.

1. Navigate to the `PizzaOrderingBot` bot\. Choose **Editor**\. and then choose **Error Handling**\.  
![\[\]](../images/gs1-80.png)

1. Use the **Editor** tab to configure bot error handling\.
   + Information you provide in **Clarification Prompts** maps to the bot's [clarificationPrompt](https://docs.aws.amazon.com/lex/latest/dg/API_PutBot.html#lex-PutBot-request-clarificationPrompt) configuration\. 

     When Amazon Lex can't determine the user intent, the service returns a response with this message\. 
   + Information that you provide in the **Hang\-up** phrase maps to the bot's [abortStatement](https://docs.aws.amazon.com/lex/latest/dg/API_PutBot.html#lex-PutBot-request-abortStatement) configuration\. 

     If the service can't determine the user's intent after a set number of consecutive requests, Amazon Lex returns a response with this message\.

   Leave the defaults\.


**Next Step**  
[Step 3 : Build and Test the Bot](ex2-step3.md)