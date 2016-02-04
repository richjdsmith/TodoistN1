# TodoistN1
Todoist Plugin for N1- add email as tasks

![](assets/Todoist Banner.png)

Screens

![](assets/screen1.png)
![](assets/screen2.png)


# Installing

1. Go to https://developer.todoist.com/appconsole.html
2. Sign in with your Todoist account
3. Click the "Create new app" button
4. Choose a name, it doesn't really matter what, but for simplicity sake, I recommend something that includes N1 in it, perhaps "TodoistN1". Go ahead and leave the other option blank then press create.
5. From this new screen, the only things you need to worry about are the Client ID, the Secret Key and that OAuth Redirect URL field. The Client ID and Secret Key are generated for you, but you need to put something in for the redirect url. You can use whatever you would like, just use something like "http://yourname.com/todoist".
6. Ignore everything else, but keep this window open, you will need it shortly.
7. Go download this plugin now from here [get](https://github.com/anopensourceguy/TodoistN1/releases) (I'm assuming you have already installed Nylas N1, if not, go do that as well!)
8. Extract the file, open the folder that you extracted and navigate to ToDoistN1 -> lib -> my-message-sidebar.cjsx and open it in your favourite text editor, I like sublime text 3.
9. Now, around line 13, you should see: client_id: "", client_secret: "", Go ahead and add in those keys from your Todoist Developers account, they are the ones that were generated for you.
10. Next, around line 128 (Or just ctrl+f/cmd+f "uri"), you should find:
.send({ client_id: options.client_id, client_secret: options.client_secret, code: code, redirect_uri: "**http://www.iamsupratim.com/n1todoist**" })
OR
.send({ client_id: options.client_id, client_secret: options.client_secret, code: code, redirect_uri: "**yourredirecturlhere**" })
Go ahead and replace either the http://www.iamsupratim.com/n1todoist or yourredirecturlhere with that OAuth Redirect URL you created on the Todoist Developers site (the place where you generated those keys).
11.  Save that file and close it.
12.  Open Nylas N1 and navigate to Developer -> Install a plugin manually...
13.  This should open a finder/explorer window. Simply direct it to the folder you extracted, for example ~/downloads/TodoistN1-1.0 and click open.
14.  Once N1 says it has installed, close the program then re-open it (Ignore what it says about not needing to close it).
15.  If you followed these steps, you should find that there is a Sign In to Todoist button on your sidebar, click it, sign in normally and give it your permissions. Ta-da!

NOTE: As of this build, after you have signed in, pressing the SEND TO TODOIST button doesn't give any indication that it did anything. Don't press it multiple times, it did work and it did send it to your Todoist account, just check under inbox and you should see your email's name sitting in you inbox, ready to be edited!
