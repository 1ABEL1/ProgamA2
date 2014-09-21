ProgamA2
========
I finished my homework in time but all this github/commit thing was too confusing, i think i have just lost 10%. 
Im so pissed right now, im just gonna copy/paste my code here, at least you will see i worked.
Here is my code:
=================
## I don´t want to get into details but i have had a very busy week. So I apologize: I 
## don´t have that much time to write comments, I hope you find clear what I do here.
## It is analogous to the vector example in coursera.


makeCacheMatrix <- function(x = matrix()) {
In<-NULL
set<-function(y){
  x<<-y
  In<<-NULL
}
  get<-function()x
  setinverse<-function(solve) In<<-solve
  getinverse<-function()In
  list(set=set,get=get,setinverse=setinverse,getinverse=getinverse)
}


##

cacheSolve <- function(x, ...) {
        ## Return a matrix that is the inverse of 'x'
  In<-x$getinverse()
  if(!is.null(In)){
    message('getting cache data')
    return(In)
  }
  data<-x$get()
  In<-solve(data,...)
  x$setinverse(In)
  return(In)
}
Coursera
