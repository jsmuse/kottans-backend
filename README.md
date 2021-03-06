# kottans-backend

<h3>Git Basics</h3>

<p>I've already done it: <a href="https://github.com/jsmuse/kottans-frontend#git-basics">Git and GitHub</a></p>

## Unix Shell

<p>I've got a lot of new information, it's been complicated and interesting. I think I don't afraid command line anymore :)</p>

<img src="./task_unix_shell/linux-survival.png" />

## Git Collaboration

<p>I've already done it: <a href="https://github.com/jsmuse/kottans-frontend#git-collaboration">Git and GitHub</a></p>

## NodeJS Basics 1

<p>learnyounode:</p>
<img src="./node_basic_1/learnyounode.png" />

<p>stream adventure:</p>
<img src="./node_basic_1/stream-adventure.png" />

<p>functional-javascript-workshop:</p>
<img src="./node_basic_1/.png" />

## Memory Management

> <p>What's going to happen if program reaches maximum limit of stack ?</p>
<p>If the maximum stack size has been reached, we have a stack overflow and the program receives a Segmentation Fault. While the mapped stack area expands to meet demand, it does not shrink back when the stack gets smaller.</p>

> <p>What's going to happen if program requests a big (more then 128KB) memory allocation on heap ?</p>
<p>The heap is enlarged via the brk() system call (implementation) to make room for the requested block.</p>

> <p>What's the difference between Text and Data memory segments ?</p>
<p>The difference between data and text memory segment is:
-Data segment is contain static variables which can be modified.
-Text segment is read-only and stores all code. </p>

```
08048000-08053000 r-xp 00000000 fc:00 1444599    /bin/cat
08053000-08054000 r--p 0000a000 fc:00 1444599    /bin/cat
08054000-08055000 rw-p 0000b000 fc:00 1444599    /bin/cat
08292000-082b3000 rw-p 00000000 00:00 0          [heap]
b73a6000-b75a6000 r--p 00000000 fc:00 921568     /usr/lib/locale/locale-archive
b75a6000-b75a7000 rw-p 00000000 00:00 0
b75a7000-b774d000 r-xp 00000000 fc:00 2227752    /lib/i386-linux-gnu/libc-2.15.so
b774d000-b774f000 r--p 001a6000 fc:00 2227752    /lib/i386-linux-gnu/libc-2.15.so
b774f000-b7750000 rw-p 001a8000 fc:00 2227752    /lib/i386-linux-gnu/libc-2.15.so
b7750000-b7753000 rw-p 00000000 00:00 0
b7758000-b775a000 rw-p 00000000 00:00 0
b775a000-b775b000 r-xp 00000000 00:00 0          [vdso]
b775b000-b777b000 r-xp 00000000 fc:00 2227760    /lib/i386-linux-gnu/ld-2.15.so
b777b000-b777c000 r--p 0001f000 fc:00 2227760    /lib/i386-linux-gnu/ld-2.15.so
b777c000-b777d000 rw-p 00020000 fc:00 2227760    /lib/i386-linux-gnu/ld-2.15.so
bf9ad000-bf9ce000 rw-p 00000000 00:00 0          [stack]
```


<p>The articals were complicated to understanding. But I figured it out :)

The last task was really difficult for me. The command in description didn’t work for my MAC, so I had to install my virtual machine with linux. And then it worked! I’ve spent a few days to understand where is a mistake. I’m afraid, I still don’t understand why is that command don’t work on my MAC :(</p>


## TCP. UDP. Network

<p>Internet 101:</p>

<img src="./task_networks/Google Chrome_2020-02-10 12-13-20@2x.png" />

<p>Networking for Web Developers:</p>

<img src="./task_networks/Google Chrome_2020-04-02 12-34-51@2x.png" />

## Http & Https

<h3>Practice:</h3>

```
curl https://api.github.com/users/jsmuse
curl -i https://api.github.com/users/jsmuse
curl  https://api.github.com/gists/starred
curl --user "jsmuse:BLABLABLA" https://api.github.com/gists/starred
curl --user "jsmuse:*" https://api.github.com/gists/starred
curl --user "jsmuse" https://api.github.com/gists/starred
```


Additional task:
```
curl -i https://api.github.com/orgs/kottans/repos

curl --user 'jsmuse' -X POST -d \
   -d '{ \
        "title": "New issue", \
        "body": "We should have one", \
      }' \
   https://api.github.com/repos/jsmuse/kottans-backend/issues
```

<h3>Questions:</h3>

> <p>Name at least three possible negative consequences of not using https:</p>

<p>Someone can eavesdrop your messages, someone can intercept and manipulate the message, you can’t identify who visits your website</p>


> <p>Explain the main idea behind public key cryptography in few sentences:</p>

<p>Any person can encrypt a message using the receiver's public key, but that encrypted message can only be decrypted with the receiver's private key.</p>


> <p>You are creating an application for pet clinic. You need to implement the following functionality:</p>

<p>POST request to add new pet. Data is sending in request body. Status code: 200 OK</p>
<p>GET request to search pet. Data is sending in request query params. Status code: 200 OK</p>
<p>PUT request to change name of an existing pet. Data is sending in request body. Status code: 200 OK</p>
<p>PUT request to add new info about pet's health. Data is sending in request body. Status code: 201 Created</p>
<p>POST request to assign a pet to a particular doctor in the clinic. Data is sending in request body. Status code: 200 OK</p>
<p>POST request to register an appointment for a pet. Data is sending in request body. Status code: 201 Created</p>

## Patterns
