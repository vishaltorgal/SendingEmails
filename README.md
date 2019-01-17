### Sending Emails in Android
- - -


[![Alt text](https://github.com/vishaltorgal/SendingEmails/blob/master/dlapk.png)](https://github.com/vishaltorgal/SendingEmails/raw/master/sendingemails.apk)

<b>

 
<img src="https://github.com/vishaltorgal/SendingEmails/blob/master/1.png " alt="alt text" width="450" height="600">
<img src="https://github.com/vishaltorgal/SendingEmails/blob/master/2.png " alt="alt text" width="450" height="600">



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
