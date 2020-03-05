# Step 3: Update the Intent: Configure a Code Hook

In this section, you update the configuration of the `MakeAppointment` intent to use the Lambda function as a code hook for the validation and fulfillment activities. 

1. In the Amazon Lex console, select the ScheduleAppointment bot. The console shows the **MakeAppointment** intent. Modify the intent configuration as follows. 
**Note**  
You can update only the $LATEST versions of any of the Amazon Lex resources, including the intents. Make sure that the intent version is set to $LATEST. You have not published a version of your bot yet, so it should still be the $LATEST version in the console.

   1. In the **Lambda initialization and validation** section, choose **Initialization and validation code hook**, and then choose the Lambda function **MakeAppointmentCodeHook** from the list.

   1. In the **Fulfillment** section, choose **AWS Lambda function**, and then choose the same Lambda function from the list.

1. Choose **Save Intent**, and then choose **Build**.

1. Test the bot.   
![](../images/appt-test-with-lambda.png)

**Next Step**  
[Step 4: Deploy the Bot on the Chatbot Webapp](ex5-step4.md)
