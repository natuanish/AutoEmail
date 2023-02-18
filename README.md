# AutoEmail
This program is a Python script that allows you to send automated emails using the Gmail API.

The script uses the oauth2client library to authenticate with the Gmail API using OAuth2. Once authenticated, it builds and sends the email message using the apiclient library.

To use this script, you need to have a client_secret.json file, which you can obtain by creating a project in the Google Developers Console and enabling the Gmail API. You also need to have the oauth2client and apiclient libraries installed in your Python environment.

The get_credentials function retrieves the credentials of the authenticated user. If the credentials don't exist or are invalid, the function launches a flow to obtain new credentials from the user. The function saves the credentials to a file for future use.

The SendMessage function is the main function that creates and sends the email. It takes the sender email address, recipient email address, subject, message body in both HTML and plain text formats, and an optional file attachment.

The SendMessageInternal function is a helper function used by SendMessage to actually send the email via the Gmail API.

The CreateMessageHtml function is another helper function used by SendMessage to create an email message with a HTML body.

The createMessageWithAttachment function is a third helper function used by SendMessage to create an email message with an attached file.

The sendmail function is the function that reads a line from the CSV file containing the recipient email address and sends an email to that address.

Finally, the main function reads the CSV file and calls the sendmail function for each line in the file. You can customize the contents of the email by modifying the msgHtml variable in the sendmail function.
