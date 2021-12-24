---
layout: post
title: Email Security Analysis
---

​​I wanted to go over in more detail how to examine an email and determine if it is malicious. 

This is a continuation of this post on phishing 
[How to Spot Phishing](https://zendannyy.github.io/ninth-post/)


### Things to analyze in a suspicious email
* Link Analysis
* Reading the headers (bottom to top)


### Link Analysis 
Most phishing attempts nowadays will come in the form of links. Ask yourself, when you hover over the link, does it match where it says it's going to? Do you spot any typos or unexpected domains?
![Example Email II](/images/Example_Email_ll.png)

Google it without accessing the domain. For example in the email above, hovering over the link shows coatpurple[.]com typing site:coatpurple.com will return results without risk of going to the actual site. 


### Reading the Headers
To do this in gmail select "Show Original" , for yahoo do "View raw message"
The reason why you read these bottom to top is because this follows the "flow" the email took to get to your inbox. By following it, you can see if the email flow makes sense. 
Specifically, look at the *From:* field to verify the sender, and the *Received:* field to follow the route. 
![Example Email Headers](/images/Example_Headers.png)

As you can see in this example, the *Received:* field gives the IP address as well as the sender domain. The next Received going up talks about the SPF(Sender Policy Framework) record and it then going to 


I hope this helps in determining for yourself what is a phishing email when you see one 
