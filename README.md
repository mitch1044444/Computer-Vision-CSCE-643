# GitHub Introduction
## You will learn how to:
1. Create and use a repository
2. Start and manage a new branch
3. Make changes to a file and push them to GitHub as commits
4. Open and merge a pull request

## What is github?
Github is a plataform for version control and collaboration [1](https://guides.github.com/activities/hello-world/). In other words, It is a  easy way to keep track of the story of your files project and if necessary to undo the changes.

## Let's start
### Step 1: Log In
Log in into [GitHubTamu](https://github.tamu.edu/) with your netId and password.
### Step 2: Create a Repository.
A repository is usually used to organize a single project. [1](https://guides.github.com/activities/hello-world/). It can be either public or private. Public means everybody can see it and collaborate and private only you and people you invite to collaborate can see it.

1. Click on "Start a project" or "New Repository".
2. Name your repository "CSCE-315-Lab1"
3. Write a short description
4. Select Public
5. Optional: Mark Initialize this repository with a README and Add .gitignore: C++.
6. Click on "Create repository".

You have created your first project in Github. Now It is time to work with it.

### Step 3: Clone the project.
#### By command Line.
Open your terminal and go to your project directory with the command `cd`
Write the following command
```
git clone <URL>
```
To get the URL of your project: In the website of your project click on "Download or Clone", copy/paste the URL

#### Desktop options
There are several git software to use. You can download and use whatever you like.([GitHub Desktop](https://desktop.github.com/), [SourceTree](https://www.sourcetreeapp.com/)), add your remote repository, then clone it to local machine.

###Step 4: Status
The status as the name suggests, it is used to see the status of our local copy of the project
In other words, to see whether we have added a new file, deleted a file or modified a file
```
git status
```
### Step 5: Modify your project.
Open your [Visual Studio IDE and create a C++ project](https://msdn.microsoft.com/en-us/library/ms235629.aspx) or any other Code Editor you prefer.

You can copy this code. Taken from: [2](http://fahad-cprogramming.blogspot.com/2014/05/bubble-sort-in-c-code-example.html)
```c++
#include<iostream>
using namespace std;

int main(){
     //declaring array
      int array[5];
      cout<<"Enter 5 numbers randomly : "<<endl;
      for(int i=0; i<5; i++)
      {
     //Taking input in array  
       cin>>array[i];        
      }  
      cout<<endl; 
      cout<<"Input array is: "<<endl;
      
      for(int j=0; j<5; j++)
      {
       //Displaying Array 
       cout<<"\t\t\tValue at "<<j<<" Index: "<<array[j]<<endl;         
      }   
      cout<<endl;
    // Bubble Sort Starts Here
     int temp;
     for(int i2=0; i2<=4; i2++)
   {
     for(int j=0; j<4; j++)
     {
        //Swapping element in if statement    
           if(array[j]>array[j+1])
       {
        temp=array[j];
        array[j]=array[j+1];
        array[j+1]=temp;        
       }
     }         
   } 
   // Displaying Sorted array
      cout<<"  Sorted Array is: "<<endl;
     for(int i3=0; i3<5; i3++)
   {
    cout<<"\t\t\tValue at "<<i3<<" Index: "<<array[i3]<<endl;  
   }   
return 0;
}
```
Notice that: This code is in your local project and It is not in you online repository.

### Step 6: Add files into your repository
First we have to inform to git that the project have chaged, adding this file with the command ``` git add```

To add a single file:
```bash
git add <filename>
```
or to add all the files:
```bash
git add .
```

Now we need to commit those changes with the command 
```
git commit -m "a message with the changes"
```
With this two commands we inform to git that something has changed, but we have not upload it to our online respository.

To upload the changes we do

```
git push
```
Now we have modified our project locally and we have updated our repository.

### Step 7: Update your local project.
Imagine you are a team member for a project, many people are working in the same project so they can change the project too. We have to update our local version of the project when it is necessary. We know how to clone the project, with the command ``` git clone <URL>``` however we do not want to clone because we have a version of it. What we want it is to update it. 

To update your local project to match the online go to your local project directory and write:

```bash
git pull
```
We usually check the status of the project to see if we need to pull it 

```bash
git status
```

### Step 8: Branches
Branching is the way to work on different versions of a repository at one time 

By default your repository has one branch named ```master``` which is considered to be the definitive branch. We use branches to experiment and make edits before merging them to ```master```. [1](https://guides.github.com/activities/hello-world/)

#### Step 8.1: Create a branch
##### Using githubTamu site
1. Go to your repository
2. Click the drop down at the top of the file list that says branch: master.
3. Type a branch name into the new branch text box.
4. Select the blue Create branch box or hit “Enter” on your keyboard.

##### Command Line

```bash
git brach <branch-name>
```

To see all the project branches

```bash
git brach
```

### Step 8.2: Checkout Branch
As soon as we create a branch It is necessary to "log in" into it. If we do not do it, every change will be done in ```master``` branch.

```bash
git checkout <branch-name>
```

### Step 8.3: Merge

When we are sure about the branch feature we have been working on. It is necessary to merge with the ```master```.

```bash
git merge <branch-name>
```
This command will merge our branch with its branch's father.\

## Add Contribuitors
1. Go into settings menu > Contribuitors
2. Add a user with her/his tamu email
3. Both Clone the project
4. Both Push files into the repository

## References
1.  [Github Hello World](https://guides.github.com/activities/hello-world/) 
2.  [Bubble sort](http://fahad-cprogramming.blogspot.com/2014/05/bubble-sort-in-c-code-example.html)
















