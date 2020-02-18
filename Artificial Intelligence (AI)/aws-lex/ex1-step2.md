# Step 2: Create a Lambda Function \(Console\)<a name="ex1-step2"></a>

Create a Lambda function \(using the **lex\-order\-flowers\-python** blueprint\) and perform test invocation using sample event data in the AWS Lambda console\.

You return to the Amazon Lex console and add the Lambda function as the code hook to fulfill the `OrderFlowers` intent in the `OrderFlowers` Bot that you created in the preceding section\.

**To create the Lambda function \(console\)**

1. Sign in to the AWS Management Console and open the AWS Lambda console at [https://console\.aws\.amazon\.com/lambda/](https://console.aws.amazon.com/lambda/)\.

1. Choose **Create function**\.

1. On the **Create function** page, choose **Use a blueprint**\. Type **lex\-** in the filter text box and then press `Enter` to find the blueprint, choose the `lex-order-flowers-python` blueprint\.

   Lambda function blueprints are provided in both Node\.js and Python\. For this exercise, use the Python\-based blueprint\.

1. On the **Basic information** page, do the following\.
   + Type a Lambda function name \(`OrderFlowersCodeHook`\)\.
   + For the execution role, choose **Create a new role with basic Lambda permissions**\.
   + Leave the other default values\.

1. Choose **Create function**\.

1. Test the Lambda function\.

   1. Choose **Select a test event**, **Configure test events**\.

   1. Choose **Amazon Lex Order Flowers** from the **Event template** list\. Give the test event a name \(`LexOrderFlowersTest`\)\.

   1. Choose **Create**\.

   1. Choose **Test** to test the code hook\.

   1. Verify that the Lambda function successfully executed\.

**Next Step**  
[Step 3: Add the Lambda Function as Code Hook \(Console\)](ex1-step3.md)
