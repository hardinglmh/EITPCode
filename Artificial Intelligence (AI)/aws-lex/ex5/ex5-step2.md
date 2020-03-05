# Step 2: Create a Lambda Function

In this section, you create a Lambda function using a blueprint ([**lex-make-appointment-python**](../source/lex-make-appointment-python.js)) that is provided in the Lambda console. You also test the Lambda function by invoking it using sample Amazon Lex event data that is provided by the console.

1. Sign in to the AWS Management Console and open the AWS Lambda console at [https://console.aws.amazon.com/lambda/](https://console.aws.amazon.com/lambda/).

1. Choose **Create a Lambda function**.

1. For **Select blueprint**, type **lex** to find the blueprint, and then choose the **[**lex-make-appointment-python**](../source/lex-make-appointment-python.js)** blueprint.

1. Configure the Lambda function as follows, and then choose **Create Function**.
   + Type the Lambda function name (`MakeAppointmentCodeHook`).
   + Leave other default values.

1. Test the Lambda function.

   1. Choose **Select a test event, Configure test events**.
   
   1. Choose **Amazon Lex Make Appointment** from the **Event template** list. Give the test event a name ([`LexMakeAppointmentTest`](../source/lex-make-appointment-test.json)).

   1. Choose **Create**.

   1. Choose **Test** to test the code hook.

   1. Verify that the Lambda function successfully executed. The response in this case matches the Amazon Lex response model.

**Next Step**  
[Step 3: Update the Intent: Configure a Code Hook](ex5-step3.md)
