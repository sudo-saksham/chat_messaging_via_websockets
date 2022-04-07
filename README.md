+ Chat Messaging via WebSocket
Integrating ChatMessaging via WebSocket (socket_io package) in Flutter Application

To run this application, there are 3 parts :

**1. Running the server**

**2. Resolving localhost issue (for testing on localhost)**

**3. Running client**

**4. Testing application**

> **1. Running the server**

  1. Go to the `chat_server` directory
  2. Execute `dart run` in the directory
  3. Server should run successfully on localhost.


> **2. Resolving localhost issue (for testing on localhost)**
  
**Question : Why do you face this issue?**
  
**Answer** : For testing we need 2 clients, I for myself took one as my own mobile phone and other the chrome on the current system. 
Now, when we run the server and the client will try to connect to the server (on mobile phone) it'll be through phone's localhost itself and not the system's localhost on which the server is actually running. 
Therefore, it'll show an `Connection refused Error`. To resolve this issue this section is important.
  
  Execute the following command :
  `adb reverse tcp:3000 tcp:3000`
  
  > **3. Running client**
    
   1. Goto the `chat_client` directory
   2. Run `flutter run` to run it on phone.
   3. Parallely, run `flutter run -d chrome` to run the other client on Chrome.
 
 > **4. Testing application**
 
   1. Login with any of the following dummy user name: `Ashwin`, `Shourya`, `Ayush`, `Kunal`, `Piyush`, `Saksham` (case sensitive).
   2. Click the login button.
   3. You'll see a list of Chat users on the application after logging in.
   4. Now, **on the other client** login with any dummy chat user.
   5. Open the corresponding chat of the user logged in other client. 
      (Let's say, I logged in with `Ashwin` on phone and `Saksham` on chrome. 
      Then, click `Saksham` on the phone to open chat of `Ashwin` with `Saksham` and open `Ashwin` chat on chrome)
   6. Now, type a`message`and click send icon on client, you should see the message on both clients.
   
   If you're able to successfully run all the steps then congratulation you've successfully run Chat Messaging application. 🥳🥳
   
   Checkout the code, and raise an issue if you have any doubt.
