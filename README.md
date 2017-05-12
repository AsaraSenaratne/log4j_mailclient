# log4j_mailclient
Send email using log4j in Java

Create a Java project.
Add the log4j.properties file into the src directory.
Provide email addresses and password as required in the below places.

    log4j.appender.sendMail.To=<give an email address>
    log4j.appender.sendMail.From=<give an email address>
    log4j.appender.sendMail.SMTPUsername=<give any email address>
    log4j.appender.sendMail.SMTPPassword=<password of the email address provided above>

When sending Emails, the SMTP protocol is used and it is advised to use port 465 if the mail client is gmail

    log4j.appender.sendMail.SMTPProtocol=smtps
    log4j.appender.sendMail.SMTPPort=465

In the .java file add the below line after class declaration out of the method declarations.

    private static Logger logger = Logger.getLogger(Mailer.class);
 
Where "Mailer" in 'Mailer.class' reflects the class name of the .java file






