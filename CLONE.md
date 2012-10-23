# Cloning Instructions

## Stuff to do before you formally setup your team

1. Each person on the team needs to register an account on GitHub.

2. First, you need to follow the instructions from GitHub on how to 
generate an SSH public and private keys at: https://help.github.com/articles/generating-ssh-keys.
 You need to follow the steps in that help page for every computer that you 
wish to be able to work on the project from. If you do this on <code>nike</code> then
you will be able to work on the project from <code>nike</code> and the iMacs in the
Boyd 307 lab.

## Stuff to do after you formally setup your team

2. In order to clone the repository and set everything up correctly, first write
down the URL for the <code>git</code> repository that has been setup for your
team in the space below:

````markdown

git@github.com:mepcotterell-cs1302/

````

3. Login to your <code>nike</code> account and use the following commands to clone the
repository:

````
$ git clone git@github.com:mepcotterell-cs1302/cs1302-minesweeper.git LastName-LastName-p3
$ cd LastName-LastName-p3
$ git remote add upstream <insert private repos url here>
$ git push -u upstream master
````

4. Start working!

## Notes

Now when you <code>push</code> or <code>pull</code>, your committed changes will go to your
private repository on GitHub!

If an update to the skeleton code is announced then you need to issue the following
command from withing the project directory in order to make sure that you are 
pulling from the appropriae place:

````
$ git pull git@github.com:mepcotterell-cs1302/cs1302-minesweeper.git
````

If you have any questions then feel free to email <code>mepcotterell+1302@gmail.com</code>.