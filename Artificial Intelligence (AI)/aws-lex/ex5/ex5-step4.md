# Step 4: Deploy the Bot on the Chatbot Webapp

In the preceding section, you tested the `ScheduleAppointment` bot using the client in the Amazon Lex console. To test the dynamically generated response cards that the bot supports, deploy the bot on the Chatbot Webapp and test it.

1. Copy [`aws-lex-bot-wizard`](../source/aws-lex-bot-wizard) folder to project.
1. Just add following markup to any page or add new html file with this content:
  ```
  <script>
    fullPage = false;
    chatbot_identifier = 'chatbot-widget';
    botName = '<lex-bot>'
    awsRegion = '<aws-region>'
    awsCognitoPoolId = '<aws-cognito-pool>'
  </script>
  <div id="chatbot-widget" data-username="Hey User">
  <script src="bundle.min.js"></script>
  ```
  Change the `botName`, `awsRegion`, `awsCognitoPoolId` and bundle file path.
  
 [Widget HTML](../source/aws-lex-bot-wizard/widget.html) with `ScheduleAppointment` Bot for your reference.

**Next Step**  
[Details of Information Flow](ex5-step5.md)