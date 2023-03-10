# H1 First week exercises.

## 1

A summary of the given topic and other assignments.

**Intrusion-Kill-Chain:**
- A kill chain is a systematic way to confront an adversary and produce the desired results. In this research, a novel kill chain model for invasions is presented.
- It includes reconnaissance, weaponization, delivery, exploitation, installation, command and control, and actions on objectives. 
- Email attachments, web sites and USB removable media are the most common delivery vectors for weaponized payloads by APT actors.
-  Increasingly, client application data files such as Adobe Portable Document Format (PDF) or Microsoft Office documents serve as the weapon's payload.

**Courses-of-Action:**
- When defenders match enterprise capabilities to the precise methods an adversary employs to target that enterprise, the intrusion kill chain becomes a model for actionable intelligence.
- Defenders can measure the performance as well as the effectiveness of these actions, and plan investment roadmapsto rectify any capability gaps. To better safeguard their own system, defenders might use intrusion kill chain to think like attackers.
- Table 1 depicts a course of action matrix using the actions of detect, deny, disrupt, degrade, deceive, and depicts in the exploitation phase, for example, that host intrusion detection systems (HIDS) can passively Illustrating the spectrum of capabilities defenders can employ, the matrix includes traditional systems like network intrusion detection systems (NIDS) and firewall access controladversaries that continually adapt their operations over time.particularly previously undisclosed “zero-day” exploits.
- Defenders can generate metrics of this resiliency by measuring the performance and effectiveness of their defenses against intruders.
- In December, defenders detect the weaponization and block the delivery but uncover a brand new, unmitigated, zero-day exploit in the process. In March, the adversary re-uses the same exploit, but evolves the weaponization technique and delivery infrastructure, circumventing detection and rendering By June, the defenders updated their capabilities sufficiently to have detections and mitigations layered from weaponization to C2. kill chain, defenders had the proper perspective of the relative effect of their defenses against the intrusion

*My thoughts*
- A security risk exists whenever a computer is connected to a network. 
- Nobody can ensure 100% safety. But we can always lessen the damage.
- Is there ever going to be a moment when information is completely safe?

## 2

**Karvinen 2020: Command Line Basics Revisited**

This was a fairly nice review read because I just finished my server technologies course, where we had to use the same commands in the Ubuntu server. I did discover some new commands that were useful.


## A) Bandit oh-five.

Our task was to solve level 0-4.(Mandatory) in the [Over The Wire Games](https://overthewire.org/wargames/bandit/bandit0.html)

First i installed the ssh server using the command 

``` sudo apt install openssh-server ```

then I used the command `ssh bandit0@bandit.labs.overthewire.org -p 2220`to connect, `-p` here refers to the port number. 


<img width="584" alt="band0" src="https://user-images.githubusercontent.com/102954934/214156949-ffb1c0bf-703c-4ee3-9685-3a1d934ad3f8.png">

We can see the image above that shows the mainpage. After completing the first level we must exit inorder to continue to the next one. So, continuing to lvl 1 I connected with the same command that i used before `ssh bandit0@bandit.labs.overthewire.org -p 2220` but instead of bandit0 I used bandit1 and it was pretty much same with bandit3 and bandit4, just had to exit after every successful connection.

*level 0 password:*

<img width="262" alt="band0pw" src="https://user-images.githubusercontent.com/102954934/214163918-8665eb0a-46f4-437f-bfba-46d4407dee91.png">

Here I used `cat` to find out the password.

*level 1 password:*

<img width="311" alt="1 pw" src="https://user-images.githubusercontent.com/102954934/214165425-6b6a38ae-8242-425d-a25a-30707788f266.png">

Here I first used `ls` to list all the files. This one was quite tricky as the file name was `-` so I could not just use `cat -`. I tried doing that and it did not work. So then after some research I found out I had to use `cat ./-` command inorder to access the password for the next level.

*level 2 password:*

<img width="371" alt="2 pw" src="https://user-images.githubusercontent.com/102954934/214166778-06cda870-0c18-4d1a-ab88-b2456a6e94b7.png">

This one was fairly easy one, atleast for me. Just had to used `\` in the above shown manner.

*level 3 password:*

<img width="281" alt="pw3" src="https://user-images.githubusercontent.com/102954934/214171270-4ca0305e-3d95-4530-960e-2ae85c21a019.png">

For this level, first I had to change the directory and inside the directory open the .hiddenfile using `cat .hiddenfile` command.

*level 4 password:*


<img width="292" alt="pw4" src="https://user-images.githubusercontent.com/102954934/214171709-5bd9ce89-de2d-4a77-b1c4-fbd64d671c62.png">


<img width="268" alt="pw4 2" src="https://user-images.githubusercontent.com/102954934/214171723-5072db75-291e-428a-8cab-0be321cefcb6.png">

Not gonna lie, this one was troublesome. It took me sometime to figure this out. I had to figure out which file was the only human-readable file. After I found out I used the similar command `cat ./-file07` to figure out the password for next level.

## B) Bullseye: Install Debian 11-Bullseye virtual machine in VirtualBox.

This task went smoothly, I did not really have any trouble with the installation except tht fact that i could not find any install button. After 5 min of punching some random keys and moving the mouse in a crazy way, I figured out that I just had to drag it abit above then only i found the install button. Other than that, it was ok.

## C) WebGoat: Install WebGoat.

Inorder to install the webgoat I used the [Material](https://terokarvinen.com/2020/install-webgoat-web-pentest-practice-target/) provided by Tero Karvinen.
After that I downloaded and ran it using the commands `wget https://terokarvinen.com/2020/install-webgoat-web-pentest-practice-target/webgoat-server-8.0.0.M26.jar` & `java -jar webgoat-server-8.0.0.M26.jar` respectively.

Then I registered for the webgoat using the [Link](http://localhost:8080/WebGoat/)

## D) Hacker warmup: Solve these tasks on WebGoat.

- **General: HTTP Basics**
 
<img width="320" alt="magic number" src="https://user-images.githubusercontent.com/102954934/214175724-76a29909-ef44-4e47-b782-15e048d69f89.png">

I had some difficulty finding the magic number at first. Tried google/duckduckgo but nothing helped then i just randomly searched for magic number in the inpect bar and found it at last. The magic number for me was 20 , I found one of the article online where the magic number was 40. So, i guess we users have different magic numbers. 

_ **General: Developer tools**

<img width="596" alt="dev tools function" src="https://user-images.githubusercontent.com/102954934/214176371-37908337-5518-4972-982e-80487c0c44a2.png">

As an ex-javascript student this was fairly easy and understandable for me. I had no trouble with this part.

<img width="601" alt="dev tools laast" src="https://user-images.githubusercontent.com/102954934/214187751-e756685a-4a7f-4a06-be2d-4b980f12b6b0.png">

After figuring out the magic number this was a piece of cake for me. But i found something intersting, I tried findind the value without actually pressing the go button and the value i got was `foo` but when i press the button then the value changed to `numbers`.

I am pretty excited about the course. It is interesting and fun. 


## List of sources

- (https://lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdfl)
- https://terokarvinen.com/2020/command-line-basics-revisited/
- https://terokarvinen.com/2021/install-debian-on-virtualbox/
- https://terokarvinen.com/2020/install-webgoat-web-pentest-practice-target/
- https://www.youtube.com/watch?v=ff2Au8BIy_A&t=249s
- https://medium.com/@Kamal_S/owasp-webgoat-general-lesson-solutions-of-http-basics-http-proxies-developer-tools-5f62c03a7872
