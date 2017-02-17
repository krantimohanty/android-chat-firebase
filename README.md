# android-chat-firebase

Learn to build an android real time chat application using firebase database.

Read: https://firebase.google.com/docs/database/android/start/


I have developed a very basic and simple chat app in which user can login and register in the system and can do one to one chat with other users.


Firebase Security Rules:
By default only authenticated user can access the database. When you will go to Rules tab in firebase console project then it may look like this.

{
  "rules": {
    ".read": "auth != null",
    ".write": "auth != null"
  }
}

When you try to run the app you may get authentication failure error.

So change rules to as shown below.


{
  "rules": {
    ".read": true,
    ".write": true
  }
}

Note: Above security rules will allow anyone to read, write and edit data. That means any user can edit data of any other user. This must not be allowed. So use this security rule only for testing purpose. Don’t use it if you are making the app live in market. To learn more about firebase security rules visit below link.

https://firebase.google.com/docs/database/security/
