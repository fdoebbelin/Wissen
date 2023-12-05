At times, when you commit some changes to say a remote private repo, The git asks for your credentials so that it can verify if it’s actually you who is committing these changes! This can be simplified by using GIT Credentials. It basically stores your credentials in a safe manner(encrypted) so that you don’t always have to enter your details. So in this tutorial, we will look into how to make workaround easier with GIT Credentials.

### How to setup GIT Credentials

**Step 1:** To add your credentials for a remote server (Github, Gitlab, etc…), enter the following in the terminal:


```
> git config –-global credential.helper manager-core
```

- **credential-helper** are git programs that help you save the credentials on your device.
- **manager-core** is a credential manager for GIT, It supports authentication to GitHub, Bitbucket, and Azure Repos.

To set your username, enter the following (Change `<username>` with the preferred username):

```
> git config –global user.name <username>
```


Further, if you want to set your email, just change **user.name** to **user.email** (Change `<email>` with the preferred email),

```
> git config –global user.email <email>
```


**Step 2:** The next time you will commit/push to the repo for which you added the credentials, GIT will ask you for the credentials for that particular remote server if it is unable to find the username and password already stored.