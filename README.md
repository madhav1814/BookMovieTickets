
"Building a Conversational AI Chatbot with Amazon Lex and Lambda: A Practical Guide"




What is a ChatBot ?

“A chatbot is a computer-based program that simulates human conversations. Commonly known as digital assistants, chatbots allow humans to interact with them and make the experience a realistic one.”




Lex Bot Structure
Amazon Lex : 

Amazon Lex is a service provided by Amazon Web Services (AWS) that allows developers to create conversational chatbots with natural language understanding capabilities.

AWS Lambda :  

AWS Lambda is an event-driven, serverless computing platform provided by Amazon as a part of Amazon Web Services. It is designed to enable developers to run code without provisioning or managing servers. It executes code in response to events and automatically manages the computing resources required by that code.



~Open AWS console and Search for Amazon LEX

Create a Bot Named : MovieBookingBot



Now - Create an Intent Named BookMovie

With sample utterances

Book a Movie ticket

I want you to book a movie ticket

book me {Number} tickets in {Location}



What is a Slot ?

In Amazon Lex, a slot represents a specific piece of information that the chatbot needs to collect from the user to fulfill an intent. Slots are placeholders for data that the chatbot needs to gather in order to complete a task or provide a relevant response to the user.



what is a SlotType ?

Each slot has a type. We can create the slot type or we can use the built-in slot types.

For example for the TheaterType intent we can find the types like

IMAX,3D,MULTIPLEX,DRIVE-IN




Once again open the Console and search for AWS Lambda

Create a Lambda Function named "MovieBookingLambda"




Update the code from the Git Repository



Now Open Amazon LEX and connect it to the Lambda Function

click on TEST

Open settings -> select source as MovieBookingLambda 

select Lambda function version as $LATEST



Now test the BOT



The Bot is Working Perfectly. Now Integrate It with Whatsapp.

FOR THIS WE NEED A ACCOUNT IN twilio.com

After sign-in to twilio we need to buy a number using twilio dollars in the account



Now we have to connect the Lambda Function with the TWILIO whatsapp message sender 



Now test the Bot



To test the Bot open this Link http://wa.me/+14155238886 and send a text "join invented-replied" 



