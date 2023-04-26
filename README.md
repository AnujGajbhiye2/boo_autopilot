# boo_autopilot
This is a simple JavaScript code on how to put Boo (https://boo.world/) on auto-pilot that will keep liking till the counter runs out.

````
(function theLoop (i) {
        setTimeout(function () {
            try {
                
               window.likeUser()    
                console.log("liked people count : "+ (1001 - i) )
                
            } catch (error) {
                console.log("error encounterd")
                setTimeout(() => {}, 20000);
            }
           
            if (--i) {          
              theLoop(i);       
            }
          }, 6000);
    })(1000); // <--- change this number to the number of likes you want to send
````

# How to use this code
1. Open https://boo.world/match website
2. sign in using your account
3. copy the above code and paste it in the console (Ctrl + Shift + i)
4. Keep it open in a separate window and It should automatically start sending likes, 
