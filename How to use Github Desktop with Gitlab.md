GitHub Desktop is a fast and easy way to contribute to projects from Windows and OS X, whether you are a seasoned user or new user, GitHub Desktop is designed to simplify all processes and workflow in your GitHub. 
GitHub Desktop is an open-source Electron-based GitHub app. It is written in TypeScript and uses React.

> source : [https://www.techefeed.com/internet/get-started-github-desktop/](https://www.techefeed.com/internet/get-started-github-desktop/)

It has many awesome features like:
1. Attributing commits with collaborators easily
2. Checkout branches with pull requests and view CI statuses
3. Syntax highlighted diffs
4. Expanded image diff support
5. Extensive editor & shell integrations
6. It’s open-source

I personally prefer to use Github Desktop as my main git client rather than Source Tree or Gitkraken.

Last week, the [company](https://legalrobot.com/) I work for, decided to move all it’s codebase from Github to [Gitlab](https://gitlab.com/). The reason is that Gitlab has some out of the box Features like integrated DevOps inbuilt into their system, unlike Github where you’ll have to do all these yourselves.

Pre-gitlab we were using like 5 different tools and the complexity of integrating them all was getting out of hand and also quite expensive, trying to tie together New Relic, Codeship, Github, Jenkins, Chef, and Terraform was no fun… not to mention Digital Ocean, AWS, Azure, and MongoDB Cloud

I am used to the GitHub environment because that’s all I’ve always worked with but I saw this as a challenge to adapt to a new environment.

I was ready to move to Gitlab but I wasn’t ready to leave GitHub Desktop, so I decided to use Gitlab and GitHub Desktop. I began making research on how to use them both.

So I’ll show you how to use GitHub Desktop with a Gitlab Repo that has 2FA(two-factor authentication) enabled.

So let’s visit the steps from scratch.

> Disclaimer: These steps are valid for only users of the GitHub Desktop Native

**Step one:**
i. Download GitHub Desktop [here](https://desktop.github.com/)
ii. Go to your Gitlab repo
iii. Click on settings

![](https://miro.medium.com/v2/resize:fit:700/1*w3soMTEc5K0Q0iCzadv3qQ.png)

Circled settings

**Step two:**
What we’ll do now is to generate an access token for our GitHub desktop.
After clicking on settings
i. Click on Access Tokens

![](https://miro.medium.com/v2/resize:fit:700/1*XMmRvjhDqy0XXygAJnlpTg.png)

ii. Generate an access token

![](https://miro.medium.com/v2/resize:fit:700/1*dddg6tBT8yqSPURwiPcqsA.png)

iii. Copy your new access token and store it somewhere as we’ll use it later:

![](https://miro.medium.com/v2/resize:fit:700/1*YglJK_c8xxKTwBzvj_-q_w.png)

**Step three:**
i. Head over to your repository and select https and copy the link,

![](https://miro.medium.com/v2/resize:fit:700/1*CCSybMcpqoSO2yEzEWVXDA.png)

ii. open GitHub Desktop from the file bar, select clone repository

![](https://miro.medium.com/v2/resize:fit:700/1*m9ca14FUXJJoTCfy-xN6sg.png)

iii. After selecting it, a modal would pop up, select URL and place the https link we copied from gitlab inside the URL field and select the destination folder.

![](https://miro.medium.com/v2/resize:fit:700/1*5Hs2sv0w9MHwhk8ozqp5TQ.png)

iv. After filling all those fields, select clone
v. While cloning, it would pop up a modal titled _authentication failed,_ you would then be required to put in your username and password.
**N/B:** Your username is mostly your email address or whatever username you used to access your gitlab organization or repo.
vi. Then your password would be the personal access token we created before, so head over to wherever you may have stored it and paste it.
vii. After that click login or authenticate and if all goes well you should see something like this

![](https://miro.medium.com/v2/resize:fit:700/1*iyX9y9Vt9-DOIq6VNjOIHg.png)

cloning (name of your project repo)

After that, you would see this

![](https://miro.medium.com/v2/resize:fit:700/1*QLnUBwAQtYyuwUNuG7S_3w.png)

Then you can fetch from the origin, see all branches and use it as your preferred git client.

**And that’s how to use Gitlab with GitHub Desktop.**

If you have any questions or you don’t understand any step feel free to reach out to me on [twitter](https://twitter.com/coder_blvck) or drop your questions in the comments section.

Thanks!!!