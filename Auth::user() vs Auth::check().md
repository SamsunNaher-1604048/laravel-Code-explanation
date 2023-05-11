# Laravel Auth::user() vs Auth::ckeck()
---
 we aften use ```php if (Auth::user()) {...}``` and ```php if (Auth::check()) {...}```  for same peropse, but both perpose  are different
 
 ``` php
 if (Auth::user()) {...}
 ``` 
 we use it for  get the logged in user data
 
  ```php 
  if (Auth::check()) {...}
  ``` 
  we use it to check , a user logged in or not it return bool value that means true or false.
  
  #### Intermal codding of Auth::check()
  
  Auth::check() calls Auth::user(), gets the result from it, and then checks to see if the user exists. 
  ```php
  public function check()
{
    return ! is_null($this->user());
}
  ```
 
 
 
