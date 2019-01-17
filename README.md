# Sending Emails in Android

[![Alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png)](https://github.com/vishaltorgal/SendingEmails/blob/master/sendingemails.apk)

![alt text](https://github.com/vishaltorgal/SendingEmails/blob/master/1.png =150x "Logo Title Text 1")

![alt text](https://github.com/vishaltorgal/SendingEmails/blob/master/2.png =500x "Logo Title Text 1")


```sh

    String[] TO = {""};
    String[] CC = {""};

    Intent email = new Intent(Intent.ACTION_SEND);

        email.setData(Uri.parse("mailto:"));
        email.setType("message/rfc822");
        email.putExtra(Intent.EXTRA_EMAIL, TO);
        email.putExtra(Intent.EXTRA_CC, CC);
        email.putExtra(Intent.EXTRA_SUBJECT, "Add Subject Here");
        email.putExtra(Intent.EXTRA_TEXT, "Message Body");


    try {
          startActivity(Intent.createChooser(email, "Select email client..."));
        }
    catch (android.content.ActivityNotFoundException ex) {
          Toast.makeText(MainActivity.this, "Failed", Toast.LENGTH_SHORT).show();
        }

```
