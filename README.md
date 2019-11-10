# Cake Baker

This is a learning project to administrate some order of a fictional cake company. Followed up these tutorial from [linked-in learning](https://www.linkedin.com/learning/aws-for-developers-data-driven-serverless-applications-with-kinesis/solution-sqs) Great instructor

The Arquitecture of the app is a catchin lambda of the creation of the order then another lambda to process the order reporting both reporting to kinesis, and from the kinesis data stream report trigger another function that send an e-mail to administrators.

## For running it

need to install node and npm have an AWS account and serverless framework installed. Create an IAM user with permition to run the services.

Need to get to email registered and put them on the serverless yaml, I used some teting ones

```js
npm install
sls deploy
sls remove
```

Then test the endpoints with Post man or somthing like that, it's good to remove the CF stuff just in case for you to not get charged.

## Learnings

- **kinesis**: data stream service, really good for traking real time that... wonder how it works with suscriptions.
- **Dynamo**: NoSQL service, easy api's with the aws-cli for creating and having data, not similar to mongo tho =(
- **Lambda**: Functions

Serverless infraestructure have to be well planned or you can easily lose track, passing data around all these really changes the paradigme of OOP and classes, you must catch and send data, trigger stuff but try not to change it, the instructor paid much attention to that. Thats why functional progrmaming is a must for trying to build an app with these.

Framework helps you a lot, learning how to make the yaml it's equivalent to know kubernetes, it's an art and these is where you can see a truly master into Serverless. Easy to make mistakes and lose track of what is doing stuff, the instructior didn't pay much attention into file managment but I imagine, that keeping all the stuff in the correct directory, naming conventions are a must! still as a production project I would recomend to pack functionalities.

didn't do much testing but at a first glance, really cheap. Still wach out for timing and RAM on Lambdas. Optimazing functions is olso the trick here.
