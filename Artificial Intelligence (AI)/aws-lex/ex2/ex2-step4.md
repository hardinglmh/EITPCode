# Step 4 (Optional): Clean up

Delete the resources that you created and clean up your account to avoid incurring more charges for the resources you created.

You can delete only resources that are not in use. For example, you cannot delete a slot type that is referenced by an intent. You cannot delete an intent that is referenced by a bot.

Delete resources in the following order:
+ Delete bots to free up intent resources.
+ Delete intents to free up slot type resources.
+ Delete slot types last.

**To clean up your account**

1. Sign in to the AWS Management Console and open the Amazon Lex console at [https://console.aws.amazon.com/lex/](https://console.aws.amazon.com/lex/).

1. From the list of bots, choose **PizzaOrderingBot**.

1. To delete the bot, choose **Delete**, and then choose **Continue**.

1. In the left pane, choose **Intents**.

1. In the list of intents, choose **OrderPizza**.

1. To delete the intent, choose **Delete**, and then choose **Continue**.

1. In the left menu, choose **Slot types**.

1. <a name="chooseSlots"></a>In the list of slot types, choose **Crusts**.

1. <a name="deleteSlots"></a>To delete the slot type, choose **Delete**, and then choose **Continue**.

1. Repeat [Step 8](#chooseSlots) and [Step 9](#deleteSlots) for the `Sizes` and `PizzaKind` slot types.

You have removed all of the resources that you created and cleaned up your account.
