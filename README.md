# How to setup deployment to OpenShift with Codeship

- on the codeship site navigate to: 

>Project settings > General > SSH public key

 
> Copy the contents and save to a file: (e.g.: codeship.pub)

- open a terminal and run:

>rhc sshkey add codeship codeship.pub 

- go back to the codeship site and navigate to

>Project settings > deployment > custom script

- put these lines to the deployment box

>git remote add OpenShift your_repo
>git push OpenShift master

- push to your repo ... done
