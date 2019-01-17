<h2> Sending Emails in Android <h2/>


<p style="text-align: center;"><span style="color: #000000;"><span style="caret-color: #333399;"><strong>Download APK Link&nbsp;</strong></span></span></p>
<p style="text-align: left;"><span style="color: #000000;">https://github.com/vishaltorgal/SendingEmails/blob/master/sendingemails.apk</span></p>

<br>
<p style="text-align: center;"><img src="https://github.com/vishaltorgal/SendingEmails/blob/master/1.png" alt="" width="400" height="550"/>&nbsp;</p>
<br>
<p style="text-align: center;"><img src="https://github.com/vishaltorgal/SendingEmails/blob/master/2.png" alt="" width="400" height="550"/>&nbsp;</p>


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

