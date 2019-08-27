# utl-compute-the-angle-between-twp-vectors-with-R-or-IML
Compute the angle between two vectors with R or IML
    Compute the angle between two vectors with R or IML                                                
                                                                                                       
    githib                                                                                             
    https://tinyurl.com/y6xzjgax                                                                       
    https://github.com/rogerjdeangelis/utl-compute-the-angle-between-two-vectors-with-R-or-IML         
                                                                                                       
    Stackoverflow                                                                                      
    https://stackoverflow.com/questions/1897704/angle-between-two-vectors-in-r                         
                                                                                                       
    Graeme Wals profile                                                                                
    https://stackoverflow.com/users/2024186/graeme-walsh                                               
                                                                                                       
     *_                   _                                                                            
    (_)_ __  _ __  _   _| |_ ___                                                                       
    | | '_ \| '_ \| | | | __/ __|                                                                      
    | | | | | |_) | |_| | |_\__ \                                                                      
    |_|_| |_| .__/ \__,_|\__|___/                                                                      
            |_|                                                                                        
    ;                                                                                                  
                                                                                                       
     Formula for computing theta                                                                       
                                                                                                       
      ||x|| * ||y|| * cos(theta) = x . y                                                               
                                                                                                       
                        x . y                                                                          
      cos(theta) =  -------------                                                                      
                    ||x|| * ||y||                                                                      
                                                                                                       
                (1,sqrt(3))                                                                            
                 ^|                                                                                    
                / |                                                                                    
               /  |                                                                                    
           2  / 30|                                                                                    
             Y    |                                                                                    
            /     | sqrt(3)                                                                            
           /      |                                                                                    
          / 60  90|                                                                                    
         +---X---->                                                                                    
      (0,0)      (1,0)                                                                                 
             1                                                                                         
                                                                                                       
      Dot product of x and y =                                                                         
                                                                                                       
        magnitude of x times the magnitude of y times the cosine of the angle between x and y          
                                                                                                       
     Note  ||y|| = magintude(y) = lenght of y vector =  2                                              
                                                                                                       
      ||x|| * ||Y|| cos(theta) = x . y                                                                 
                                                                                                       
       2    *   1   cos(theta) =  1  0 dot  1        =  1 * 1 + 0 * sqrt(3) = 1                        
                                            sqrt(3)                                                    
      2 * cost(theta) = 1                                                                              
                                                                                                       
      cos(theta)  = 1/2                                                                                
                                                                                                       
      theta = 60 degrees                                                                               
                                                                                                       
     *           _               _                                                                     
      ___  _   _| |_ _ __  _   _| |_                                                                   
     / _ \| | | | __| '_ \| | | | __|                                                                  
    | (_) | |_| | |_| |_) | |_| | |_                                                                   
     \___/ \__,_|\__| .__/ \__,_|\__|                                                                  
                    |_|                                                                                
    ;                                                                                                  
                                                                                                       
      %put angle between vectors= &angle;                                                              
                                                                                                       
      angle between vectors= 60.00002145385 degrees                                                    
                                                                                                       
    *                                                                                                  
     _ __  _ __ ___   ___ ___  ___ ___                                                                 
    | '_ \| '__/ _ \ / __/ _ \/ __/ __|                                                                
    | |_) | | | (_) | (_|  __/\__ \__ \                                                                
    | .__/|_|  \___/ \___\___||___/___/                                                                
    |_|                                                                                                
    ;                                                                                                  
                                                                                                       
    %utl_submit_r64('                                                                                  
       library(geometry);                                                                              
       x <- as.matrix(c(1,0));                                                                         
       y <- as.matrix(c(1,sqrt(3)));                                                                   
       dot.prod <- dot(x,y);                                                                           
       norm.x <- norm(x,type="2");                                                                     
       norm.y <- norm(y,type="2");                                                                     
       theta <- acos(dot.prod / (norm.x * norm.y));                                                    
       angle=paste(as.numeric(57.2958 * theta));                                                       
       writeClipboard(angle);                                                                          
    ',returnvar=angle);                                                                                
                                                                                                       
    %put angle between vectors= &angle degrees;                                                        
                                                                                                       
                                                                                                       
                                                                                                       
