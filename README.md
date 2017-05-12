# log4j_mailclient
Send email using log4j in Java

Create a Java project.
Add the log4j.properties file into the src directory (get a clone of the file provided here and do changes as necessary).
Provide email addresses and password as required in the below places.

    log4j.appender.sendMail.To=<give an email address>
    log4j.appender.sendMail.From=<give an email address>
    log4j.appender.sendMail.SMTPUsername=<give any email address>
    log4j.appender.sendMail.SMTPPassword=<password of the email address provided above>

When sending Emails, the SMTP protocol is used and it is advised to use port 465 if the mail client is gmail

    log4j.appender.sendMail.SMTPProtocol=smtps
    log4j.appender.sendMail.SMTPPort=465

The activities that take place through log4j gets recorded in a log file named "logfile". process of making a log in the log file is listed in the below process.

    log = logfile
    log4j.appender.file=org.apache.log4j.FileAppender
    log4j.appender.file.File=${log}/log.txt 
    log4j.appender.file.ImmediateFlush=true
    log4j.appender.file.Append=true
    log4j.appender.file.layout=org.apache.log4j.PatternLayout
    log4j.appender.file.layout.ConversionPattern=%d{yyyy-MM-dd HH:mm:ss} %-5p %c{1}:%L - %m%n

In the .java file add the below line after class declaration out of the method declarations.

    private static Logger logger = Logger.getLogger(Mailer.class);
 
Where "Mailer" in 'Mailer.class' reflects the class name of the .java file. For the above line to work import log4j.logger

    import org.apache.log4j.Logger;
    







