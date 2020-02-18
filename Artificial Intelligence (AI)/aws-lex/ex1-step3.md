# Step 3: Add the Lambda Function as Code Hook \(Console\)<a name="ex1-step3"></a>

In this section, you update the configuration of the OrderFlowers intent to use the Lambda function as follows:
+ First use the Lambda function as a code hook to perform fulfillment of the `OrderFlowers` intent\. You test the bot and verify that you received a fulfillment message from the Lambda function\. Amazon Lex invokes the Lambda function only after you provide data for all the required slots for ordering flowers\.
+ Configure the same Lambda function as a code hook to perform initialization and validation\. You test and verify that the Lambda function performs validation \(as you provide slot data\)\.

**To add a Lambda function as a code hook \(console\)**

1. In the Amazon Lex console, select the **OrderFlowers** bot\. The console shows the **OrderFlowers** intent\. Make sure that the intent version is set to `$LATEST` because this is the only version that we can modify\.

1. Add the Lambda function as the fulfillment code hook and test it\.

   1. In the Editor, choose **AWS Lambda function** as **Fulfillment**, and select the Lambda function that you created in the preceding step \(`OrderFlowersCodeHook`\)\. Choose **OK** to give Amazon Lex permission to invoke the Lambda function\.

      You are configuring this Lambda function as a code hook to fulfill the intent\. Amazon Lex invokes this function only after it has all the necessary slot data from the user to fulfill the intent\.

   1. Choose **Build**\.

   1. Test the bot using the previous conversation\.

   The last statement "Thanks, your order for roses\.\.\.\.\." is a response from the Lambda function that you configured as a code hook\. In the preceding section, there was no Lambda function\. Now you are using a Lambda function to actually fulfill the `OrderFlowers` intent\.

1. Add the Lambda function as an initialization and validation code hook, and test\.

   The sample Lambda function code that you are using can both perform user input validation and fulfillment\. The input event the Lambda function receives has a field \(`invocationSource`\) that the code uses to determine what portion of the code to execute\.

   1. Select the $LATEST version of the `OrderFlowers` intent\. That's is the only version that you can update\.

   1. In the Editor, choose **Initialization and validation** in **Options**\.

   1. Again, select the same Lambda function\.

   1. Choose **Build**\.

   1. Test the bot\.

      You are now ready to converse with Amazon Lex as follows\. To test the validation portion, choose time 6 PM, and your Lambda function returns a response \("Our business hours are from ten AM to five PM\."\), and prompts you again\. After you provide all the valid slot data, the Lambda function fulfills the order\.
![\[\]](http://docs.aws.amazon.com/lex/latest/dg/images/OrderFlowers-FullLambda.png)

**Next Step**
[Step 4: Update the Intent Configuration to Add an Utterance \(Console\)](ex1-step4.md)