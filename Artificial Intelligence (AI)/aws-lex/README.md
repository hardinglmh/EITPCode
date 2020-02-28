# **Introduction**
This is a collection of Javascript-based (Node.js) and Python-based sample code that interact with the Amazon Lex which is an AWS service for building conversational interfaces into applications using voice and text.

##  Project Description
This toolkit contains sample programs based on Amazon Lex SDK, Node.js and Python 2.7, including ordering flowers, ordering a pizza, booking a hotel and other coming projects.

### Establish Connection  
Amazon Lex provides API operations that you can integrate with your existing applications. You can use any of the following options:
+ AWS Console — The console is the easiest way to get started testing and using Amazon Lex 
+ AWS SDK — When using the SDKs your requests to Amazon Lex are automatically signed and authenticated using the credentials that you provide. This is the recommended choice for building your applications.
+ AWS CLI — You can use the AWS CLI to access any Amazon Lex feature without having to write any code.

Below examples are designed for students to get familiar with Amazon Lex, simply sign into the AWS Management Console and navigate to **Lex** under the **Artificial Intelligence** category. You must have an Amazon Web Services account to start using Amazon Lex.

### Examples
### [1 : Create an Amazon Lex Bot Using a Blueprint (Order Flowers)](./ex1/README.md)
### [2 : Create a Custom Amazon Lex Bot (Order Pizza)](./ex2/README.md)
### [3 : Create a Multiple Intents Supported Bot (Book Trip)](./ex3/README.md)
### [4 : Integrate Your Amazon Lex Bot with Static Web Page](./ex4/README.md)

### Restrictions
Q: How many languages are supported on Amazon Lex?  
A: Currently, Amazon Lex supports **US English**.

Q: Can I access Amazon Lex bots locally i.e. without an Internet connection?  
A: **No**. End users will need to access the Amazon Lex runtime endpoint over the Internet.

Q: What is the maximum duration of speech input?  
A: Amazon Lex supports up to **15 seconds** of speech input.

### Reference  
For more information about Amazon Lex, please feel free to visit the following links:  
https://aws.amazon.com/lex/  
https://aws.amazon.com/lex/faqs/  
https://docs.aws.amazon.com/lex/
