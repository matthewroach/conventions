**The file you are editing should look like one person has created it. This makes it as easy as possible for developers to read and edit each other’s code. Following the coding standards detailed below ensures that.**

---

_Based on my use of OpenBD._

## General
* Similar to the other conventions apply where able
* Use single quotes
* Use JavaScript spacing for functions/ if/ for loop etc

## Variables

* Always assign variables to a scope when possible. This is not possible outside of functions in CFM pages
* When access variables scopes such as application, url, request, cgi, variables, local use uppercase eg:  

```
URL.s / APPLICATION.environment
```

* Use the SUPER scope when you are calling a function that’s in a component extended from the current one, eg:

```
SUPER.getUser();
```


## Functions

* Always set the returntype
* output to false
* Set access type
* Arguments should have type set, required set where needed, and default if applicable


## Components 

* Either full script or full tag component, do not cross the streams
* Use tag based components for database and mail components
