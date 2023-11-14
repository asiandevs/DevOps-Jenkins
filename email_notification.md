Configuring Email Server in Jenkins using SMTP gmail

## 1. Install the Email Extension Plugin:

- Go to Jenkins Dashboard.
- Navigate to "Manage Jenkins" > "Manage Plugins."
- Install the **Email Extension Plugin** if you haven't already.

## 2. Authentication:

- For Gmail, set up an **"App Password"** because Gmail doesn't allow less secure apps to access your account directly.
- Go to your Google Account settings, navigate to "Security," and generate an "App Password" for Jenkins.
- Use this App Password as your Jenkins SMTP password.

## 3. Configure SMTP Server:

- Go to "Manage Jenkins" > "System."
- Scroll down to the **Extended E-mail Notification** section.
- Enter the SMTP server details for Gmail:
  - **SMTP Server:** smtp.gmail.com
  - **SMTP Port:** 465
  - **Default User Email suffix:** @gmail.com
  - **Use SSL:** Checked
   - **Charset:** UTF-8

## 4. Configure Jenkins System Email Address:

- Still in the "Configure System" page, find the **System Admin e-mail address** field.
- Enter your Gmail email address. This will be the sender address for Jenkins notifications.

##5. Configure Jenkins Job:

- Open the Jenkins job you want to configure.
- Click on "Configure" in the left menu.
- Scroll down to the **Post-build Actions** section.
- Add a post-build action and select **Editable Email Notification.**
- Enter the recipients' email addresses in the **Project Recipient List** field.

## 6. Advanced Email Notification:

- In the "Advanced" section of the "Editable Email Notification," you can customize the email content and subject.
- You may also choose to send emails for every unstable build or just for the first failure.

## 7. Save and Apply Changes:

- Save your changes in the Jenkins job configuration and in the global configuration.

## 8. Test Email notification:

- Do a wrong entry to fail the job and you will get a notification email.
