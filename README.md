# boo_autopilot
This is a simple JavaScript code on how to put Boo on auto-pilot that will keep liking till the counter runs out.

(function theLoop (i) {
        setTimeout(function () {
            try {
                
               window.likeUser()    
                console.log("liked people count : "+ (1001 - i) )
                
            } catch (error) {
                console.log("error encounterd")
                setTimeout(() => {}, 20000);
            }
           
            if (--i) {          // If i > 0, keep going
              theLoop(i);       // Call the loop again, and pass it 
            }
          }, 6000);
    })(1000);
