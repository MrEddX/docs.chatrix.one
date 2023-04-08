# Online Registration

<figure markdown>
   ![Register New Account](../resources/img/register.jpeg){: width="800" }
   <figcaption>Online registration form for <b>Chatrix.One</b></figcaption>
</figure>

This page allows you to self-register an **XMPP** account on this server. Your **JID** (**Jabber ID**) will be in the format `username@chatrix.one`. Please read the instructions carefully to fill in the fields correctly.
<!-- !!! failure "Important"

     At the moment, account registration, through the registration form and applications, is temporarily **suspended**! This is done in order to protect the service from bots and unscrupulous users creating multiple invalid spam profiles, which negatively affects the overall user experience. -->

<!-- <a href="javascript:history.go(-1)">Go Back</a> -->

## Username

The username **JID** (**Jabber ID**) is not case sensitive. It is recommended to use only lowercase letters. The usernames `TestUser@chatrix.one`, `testUser@chatrix.one`, `TESTuser@chatrix.one`, etc. will be interpreted as: `testuser@chatrix.one`. Special characters `"` `&` `'` `/` `:` `<` `>` `@` are not allowed in the profile name. To separate the names, you can use the characters: `.` `_` `-`. For example: `test.user@chatrix.one` or `test_user@chatrix.one` etc.

## Server

This field will be filled in automatically. No action on your part is required here.

## Password

By default, the server does not allow the use of weak passwords of the type `123456`, `abc123`, etc. I advise you to use password management software (**Password Manager**) to generate a password that is difficult to crack.

Do not tell anyone your password, not even the administrators of this **XMPP** server. You will later be able to change your password using your **XMPP** client or from the [change password page](https://chatrix.one:5280/register/change_password/).

!!! tip "Tip"

      Some **XMPP** clients can store the password on the computer, but for security reasons it is recommended that you only do this on your personal device.

  Remember your password or write it down on a piece of paper in a safe place. It is best to use password management software. In **XMPP** there is no (at least not yet) an automated way to recover the password in case you forget it. If this happens you will need to register a new account.

## Password verification

Here you will need to re-enter your chosen password. It must match what you entered in the **Password** field.

## Challenge - **CAPTCHA**

In order to protect against bots, you will need to enter the code generated in the form of an image. If your task seems too complicated, you can refresh the page to generate a new challenge.

!!! info "Information"

     In case you don't see a **CAPTCHA** code, you may have a browser extension installed that is blocking the preview. In this case, temporarily disable the extension or use a different web browser.

<!-- ## Registering a profile

!!! quote ""

    *Username:*

!!! quote ""

    *Password:*

!!! quote ""

    *Re-type Password:* -->

[Account Registration](https://chatrix.one:5280/register/new/){ .md-button }
