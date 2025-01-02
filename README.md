<h1>Active Directory Project (Home Lab) | Part 1
</h1>

<p align="center">
<img src="https://snipboard.io/WcYVU0.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<h2>Description</h2>
<br />
<p align="center">
Welcome to part one of five for the series on the active directory project. The goal of this project is to start from nothing at all to a fully functional domain environment built On-Prem. You do not want to miss out on this, because this will allow you to learn how to install and configure active directory, Splunk, and Windows machines. 
<br />
<br />
<img src="https://snipboard.io/OtBxCv.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
  For those who complete this project, this is something you can talk about during your interviews just like the other project series that I've done in the past. I am sure there will be some errors popping up for some when tackling these labs and if that does happen, I would love for you to build up your researching skills. 
<br />
<br />
<img src="https://snipboard.io/sVDS12.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
  For part one of the series, we will be focusing on creating our diagram and mapping out how we want to build out our lab logically, along with the hardware requirements. Unfortunately, if you are using an M1, M2, or M3 Mac you would be required to set this up in the cloud using a cloud provider, such as Vultur or Azure. For example, since virtualization doesn't play nice, if you have a Windows machine you can use Virtual Box to set up everything, that is what I'll use. 
<br />
<br />
<img src="https://snipboard.io/SkBvGc.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
  The main reason why we want to build out our diagram is to help understand how data might flow and how the pieces are strung up together during interviews. Some would actually provide you with a whiteboard and ask you to create a diagram of the basic lab, and hopefully by participating in this project, you will have more confidence in doing so. 
<br />
<br />
<img src="https://snipboard.io/Ae4BvI.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
To create our diagram, I'll be using a site called draw.io, as it is free to use and quick to access. Now, one thing to keep in mind is that these diagrams do not need to be pretty, you just need to do it and build it out. Later down the road, you can make it look pretty, especially if you're presenting this to a client, but if it is just a lab environment. I'd rather you focus on actually doing it versus spending hours on making it look visually appealing. 
<br />
<br />
<img src="https://snipboard.io/y06NSz.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
As for the hardware requirements, ideally, if you have a computer with at least 16 gigs of RAM and 250 gigs of disc space, you should be fine. Anything under you might experience some random issues and your machines might be extremely slow, so we'll need to adjust for that. 
<br />
<br />
<img src="https://snipboard.io/Rlfjhe.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Over to draw.io, we want to search for a server icon by clicking on "Search shapes", which we can find right here on the top left corner. Type in "server" and choose whichever icon you want. I will select the traditional server and drag it. I'll be using two servers. So one is going to be for our Splunk and another is for our active directory.
<br />
<br />
<img src="https://snipboard.io/Tp4tLF.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://snipboard.io/lfIdnk.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://snipboard.io/CDTbwj.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
So I'll just go ahead and right-click and hit "Duplicate", and now we got two servers. Let's search for "computer". I'll drag it over, then right-click and duplicate it again. Now we have two computers. One is going to be our target machine, which is a Windows 10 machine and then the other is going to be our attacker machine. 
<br />
<br />
<img src="https://snipboard.io/lnAxVP.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://snipboard.io/kMWald.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
I'll color the attacker machine as red and we can do that on the top right corner by selecting the red color. Now we can actually differentiate between the target machine and the attacker machine. The last couple of icons that I want to use is going to be a switch, router, and as well as a cloud to indicate for the internet. 
<br />
<br />
<img src="https://snipboard.io/MDvqI4.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://snipboard.io/ZiN1md.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
So let's go ahead and search for "switch". I'll click on "more results" to see what other icons exist, and I do see this one here. "L2 switch" looks pretty good, so I'll go ahead and click on that. For router, "Router" looks to pretty good too. So I'll drag and drop. For cloud, we can just select the first one. Perfect.
<br />
<br />
<img src="https://snipboard.io/OmvAsK.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://snipboard.io/SXnkta.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://snipboard.io/1CH4q8.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Now that we have our icons, we want to start connecting them. To do that, we can highlight of them, and you will see an arrow pointing up, left, down, and right. What we can do is click on the arrow and then we can just drag it onto another icon. In this case, I'm connecting it to the Switch.
<br />
<br />
<img src="https://snipboard.io/qVy7Pd.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://snipboard.io/iD2n4W.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://snipboard.io/aslyZV.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
I'll move the computer just a bit, that way we have a little bit more space. Some of the lines aren't straight, so what I can do is just drag it up, until it's straight. I'll go ahead and move the servers over on top of each other. Afterward, I'll drag it and connect it to the switch. Then, we do the same to the router. Finally, the router to the internet.
<br />
<br />
<img src="https://snipboard.io/6HoXhO.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://snipboard.io/Cx6nAk.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Now there are a couple of options that you can do that are located on the right-hand side. Now if you take a look at our connectors. For example, the router to the cloud. If you don't like that we can change the way it looks by clicking on the drop-down icon. So once I click on it, there's an option for a straight line. I'll go ahead and select that.
<br />
<br />
<img src="https://snipboard.io/U1SFr4.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://snipboard.io/xmUeBn.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://snipboard.io/lFNdjZ.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Now that the line is straight, we can just move it and won't have any of that curving action as we see on the servers. In my opinion, I like it like this since it looks a lot more cleaner. So I'll leave it as straight.
<br />
<br />
<img src="https://snipboard.io/71T4RL.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Now that we have everything connected. I'm just going to format it just a little bit, that way it looks a little bit nicer. Now I'm going to add in a our network information. So we can just double click anywhere on the screen and select "text" and I'll type in "Domain:".
<br />
<br />
<img src="https://snipboard.io/oC8yV0.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://snipboard.io/fPkE3K.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
So the domain that we're going to create is going to be called "MyDFIR". As for the network, I'll be using '192.168.10.0/24'. Our Splunk server is going to have an IP of '192.168.10.10'. Our active directory server is going to have an IP of '192.168.10.7', and lastly our attacker machine is going to have an IP of '192.168.10.250'. Just like that, we have all of our networking information right here.
<br />
<br />
<img src="https://snipboard.io/emB4R3.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Next, let's add some data to our icons. I'll just go ahead and double-click an icon and then this server will be our Splunk server. So I'll type in "Splunk Server" with the IP of '192.168.10.10". For the second server, I'll type "Active Directory", and it will have an IP of '192.168.10.7'. It will also have a Splunk Universal Forwarder. As this will allow us to send data over to our Splunk server.
<br />
<br />
<img src="https://snipboard.io/Av5bay.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
We will also have Sysmon installed that way it can collect telemetry on this server, and again send it over to Splunk. Next, is our target machine. This is going to be a Windows 10 machine that will have a DHCP-assigned IP, Splunk Universal, and Sysmon as well. As for our attacker machine, this will be Kali Linux with an IP of '192.168.10.250'; I think that's pretty good.
<br />
<br />
<img src="https://snipboard.io/JrWgt4.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://snipboard.io/g7tEXH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
So I'm going to draw another line over to our Splunk server to indicate that it is forwarding data over to our Splunk server. I am going to change this line to a dotted line by clicking on this drop-down right here. Once we click on the drop-down, we'll see a dotted line at the very bottom that's the one I'm going to be using.
<br />
<br />
<img src="https://snipboard.io/YskoQL.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>\
<br />
<br />
<img src="https://snipboard.io/wvRGbN.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://snipboard.io/9P8Ot4.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
So I'll select none and I will select "Straight". For color, I'll select green. Let's do the same for our active directory server since we are sending data over to Splunk. So I'll go ahead and connect our line there and change it to a dotted line. Change this straight, even though it's already straight, and remove the arrow. 
<br />
<br />
<img src="https://snipboard.io/pTa8R4.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://snipboard.io/3fBGtn.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://snipboard.io/lwh7SD.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
So this dotted line will indicate our forwarding of logs over to Splunk. We aren't going to forward anything from Kali over Splunk, so we don't need to connect anything from there. If we did have a firewall, we could be sending data over to Splunk via Syslog on Port '514', but we don't have a firewall so we'll just leave it as it is.
<br />
<br />
<img src="https://snipboard.io/OPzUa1.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
One last thing I forgot about was the target machine. I'm also going to be installing Atomic Red Team as well. 
<br />
<br />
<img src="https://snipboard.io/GK4V79.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Just a nice little recap here. We will be using Sysmon to help with telemetry and this will be installed on both active directory and our target machine. These will also have Splunk Universal forwarder installed to send data back to Splunk. Lastly, our target machine will have Atomic red team just in case we want to generate some interesting data down the road. Now all of the setup and installation of these tools will be in part three of the series. With our diagram, we should now have a better understanding of how our lab is connected. Now of course, you can take it to the next level and add on an IDS, an intrusion detection system, an EDR, endpoint detection and response, or a firewall to make your lab a little bit more advanced. 
<br />
<br />
<img src="https://snipboard.io/Bi1V9b.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Hopefully, by following along you now understand that creating a diagram is quite fun and pretty easy to do. Remember, it doesn't need to be pretty, but we just need to do it and of course, have it documented somewhere. Now that we have our diagram ready to go, we will be referencing this going forward, and in this project series, I will be using a total of two servers. One for Splunk and another for the active directory. Two computers, one target machine, and one attacker machine. This will all be installed using a Virtual Box. In part two, we will be going over how to install all of our components so we can get ready for the exciting stuff later on. That is it for this part and I hope you are as excited as I am to work together on another project. Remember to stay curious and do things differently.
