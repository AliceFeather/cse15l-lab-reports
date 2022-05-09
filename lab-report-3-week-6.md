# Lab Report 3
---
<br/>

## Streamlining ssh Configuration:
---
1\. **ssh/config file**

![ssh/config](labstep1.1.PNG)
![config file](labstep1.PNG)
<br/>

- I created the config file in .ssh folder and I edit the file using VScode.
<br/>


2\. **Login using alias**

![ssh in](labstep1.2.PNG)
- I login the to my ieng6 account just using the alias that I chose, which is *ieng6Linux*. And I can login without inputting password.
<br/>

3\. **Copy file to my account**
![scp](labstep1.4.PNG)
- Copied the file **LabReportDemo.java** to the ieng6 account server using `scp` with the alias

<br/>

## Setup Github Access from ieng6
---
1\. **Public Key**

![public key](labstep2.PNG)
- The public key, which end in .pub, are stored in the local computer

![github](labstep2.2.PNG)
- The public key is also stored in Github, which is named **Personal Laptop Final**
- The other public key is the key for ieng6 machines

<br/>

2\. **Private Key**

![private key](labstep2.1.PNG)
- The private key does not end with .pub. And they are stored in local computer in ssh folder as shown above

![private key1](labstep2.3.PNG)
- The private key for ieng6 machine is stored in .ssh for ieng6 acount as shown above

<br/>

3\. **Git commit and push**

![private key](labstep2.4.PNG)
- Commit and push was done through git commands
while logging in to ieng6 account

- [Link for the resulting commit](https://github.com/AliceFeather/markdown-parser/commit/40683d03de615b1d9f2fdc25dde3b5159d783c22
)

<br/>

## Copy whole directories with `scp -r`
---

1\. **Copying whole directory**

![copy](labstep3.1.PNG)
![copy1](labstep3.11.PNG)
- The command `scp -r . cs15lsp22ajx@ieng6.ucsd.edu:~/markdown-parse` was runned
- And the whole markdown-parse directory was copied to ieng6 account

<br/>

2\. **Logging in to ieng6 to check and run tests**

![check](labstep3.PNG)
- After logging in ieng6, using the command `ls markdown-parse` to check if markdown-parse directory is successfully copied to the account server.
- The files in the directory are copied over as well
<br/>

![test](labstep3.22.PNG)
- The above picture show the compiling and running of the tests in MarkdownParseTest.java and the outputs

<br/>

3\. **Combining commands to run at once**

![commands](labstep3.3.PNG)
![output](labstep3.31.PNG)
- As you can see in the above pictures, the command: `scp -r . cs15lsp22ajx@ieng6.ucsd.edu:~/markdown-parse; ssh ieng6Linux "cd markdown-parse; /software/CSE/oracle-java-17/jdk-17.0.1/bin/javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java; /software/CSE/oracle-java-17/jdk-17.0.1/bin/java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest"` is runned
- Copying directory to ieng6 account server, logging in ieng6, and compiling and running tests were done at the same time by combining the commands together in one line using **;** and **" "**



