---
layout: post
title:      "Enter your title here"
date:       2021-08-02 01:34:00 +0000
permalink:  enter_your_title_here
---


Getting started was all well and good, now it's time ofr the nitty gritty; applicable appssss.

To send an e-mail using your Java Application is simple enough but to start with you should have JavaMail API and Java Activation Framework (JAF) installed on your machine.

You need to add mail.jar and activation.jar files in your CLASSPATH.

Send a Simple E-mail
Here is an example to send a simple e-mail from your machine. It is assumed that your localhost is connected to the Internet and capable enough to send an e-mail.

```
// File Name SendEmail.java

import java.util.*;
import javax.mail.*;
import javax.mail.internet.*;
import javax.activation.*;

public class SendEmail {

   public static void main(String [] args) {    
      // Recipient's email ID needs to be mentioned.
      String to = "abcd@gmail.com";

      // Sender's email ID needs to be mentioned
      String from = "web@gmail.com";

      // Assuming you are sending email from localhost
      String host = "localhost";

      // Get system properties
      Properties properties = System.getProperties();

      // Setup mail server
      properties.setProperty("mail.smtp.host", host);

      // Get the default Session object.
      Session session = Session.getDefaultInstance(properties);

      try {
         // Create a default MimeMessage object.
         MimeMessage message = new MimeMessage(session);

         // Set From: header field of the header.
         message.setFrom(new InternetAddress(from));

         // Set To: header field of the header.
         message.addRecipient(Message.RecipientType.TO, new InternetAddress(to));

         // Set Subject: header field
         message.setSubject("This is the Subject Line!");

         // Now set the actual message
         message.setText("This is actual message");

         // Send message
         Transport.send(message);
         System.out.println("Sent message successfully....");
      } catch (MessagingException mex) {
         mex.printStackTrace();
      }
   }
}
```

Your output should look like this;
```
$ java SendEmail
Sent message successfully....
```

Next time, I'll bring up how to do through HTML! Thanks for reading!
