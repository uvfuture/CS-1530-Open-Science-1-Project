# Open Science Grid Interface
* Aditya Mahadevan - AdityaMahadevan
* JJ Naughton - vonbearshark
* Yiran Lin - yiranl
* David Slayback - 7thStringofZhef
* Troy Taylor - ttt10
* Dan Blackford - uvfuture

### Due Date: 13 October 2015

## CS 1530 - SPRINT 2 DELIVERABLE


# Accomplishments
We continued using Slack as our primary means of communication. We also had weekly meeetings and scheduled them such that everyone had a chance to attend at least once. Slack is working well for our team because everyone can see whats going on and can easily communicate with each other. The customer is also part of our Slack channel and we can easily communcate with them to clear up any questions we have have. For example, one of our group members suggested using the Mithril JavaScript framework. Unsure if this would be allowed, we were easily able to get in contact with the technical contact, Suchandra, and clear up the issue.

One of the major challenges faced by the developers was working with new frameworks and tools. For the walking skeleton, we had compiled a basic WAR app to display static content. For this deliverable, it was important to create something that everyone could easily run and test on their system, so it had to be redeployed as a JAR. Additionally, there was still a lot of basic infrastructure work: none of the developers had used the Spring framework before, and it took a while to even figure out the basics, let alone how to properly package it or good practices. Additionally, the framework developer had never worked with web projects or any large-scale projects that required build tools like Maven or Gradle, and it took a while to work out how to use dependencies.  

We extended the walking skeleton to work with User objects. The app is now able to accept and return JSONs for many requests (though permanent changes are not made until we have linked to the PostgreSQL, and all requests are done seperately from the frontend). Features developed on the backend are: creating, updating, and deleting users, viewing one or all user's info, and logging in or logging out a user. Additionally, the User and Job classes have been defined according to their fields in the PostgreSQL database specification given by our technical contact(although it currently does not store the password or salt via SHA256). We have also begun to implement JUnit test cases using Spring's framework, though this is still in the preliminary stage due to lack of understanding. 

# User stories completed
Code available at https://github.com/CS-1530-Open-Science-1

As the customer

I want an account system with basic info (including email and phone number)

so that I can only allow users with certain credentials to use OSG


# Why we chose those user stories



# Defects found by testing

During backend development, a recurring issue was that the id counter would fail to increment, and any new user created without an id field would overwrite the old one. This issue was resolved by switching the id field from a BigInteger to a long; however, if it becomes necessary to have larger id fields, a more permanent solution may have to be found.
Static resources would fail to display; this was fixed by storing the resources under a specific folder and changing the build path. 
