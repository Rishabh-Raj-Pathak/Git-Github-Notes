### Git Blame
================

It is a powerful command in Git that helps you identify who made changes to a specific file or line of code. Here's how to use it:

#### Basic Syntax
git blame <filename>

#### What does Git Blame do?
`git blame` shows you a detailed report of who made changes to each line of code in the specified file. It displays the following information:

* **Commit hash**: The unique identifier of the commit that introduced the change.
* **Author**: The name and email of the person who made the change.
* **Date**: The date and time when the change was made.
* **Line number**: The line number in the file where the change was made.
* **Code**: The actual code that was changed.

#### Example Output
##### Index.js
git blame Index.js
f82a2882 (Rishabh Raj Pathak 2024-07-07 22:11:31 +0530 1) 
  const name1 = "Rishabh";

f82a2882 (Rishabh Raj Pathak 2024-07-07 22:11:31 +0530 2) 
  const name2 = "Rishabh";

f82a2882 (Rishabh Raj Pathak 2024-07-07 22:11:31 +0530 3) 
  const age = "20";

^edbdce3 (Rishabh Raj Pathak 2024-07-07 22:07:41 +0530 4) 
  console.log("connected to git");

^edbdce3 (Rishabh Raj Pathak 2024-07-07 22:07:41 +0530 5) 

f82a2882 (Rishabh Raj Pathak 2024-07-07 22:11:31 +0530 6) 
  const date = "17-99-99";

f82a2882 (Rishabh Raj Pathak 2024-07-07 22:11:31 +0530 7) 

f82a2882 (Rishabh Raj Pathak 2024-07-07 22:11:31 +0530 8) 
  function isAbove18(age){
f82a2882 (Rishabh Raj Pathak 2024-07-07 22:11:31 +0530 9) 
    return age;
f82a2882 (Rishabh Raj Pathak 2024-07-07 22:11:31 +0530 10) 
}

##### newFile.js
git blame newFile.js
^edbdce3 (Rishabh Raj Pathak 2024-07-07 22:07:41 +0530 1) 
  function add(a,b){
^edbdce3 (Rishabh Raj Pathak 2024-07-07 22:07:41 +0530 2) 
    return a+b;
^edbdce3 (Rishabh Raj Pathak 2024-07-07 22:07:41 +0530 3) 
}
