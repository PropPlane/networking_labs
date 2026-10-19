# Objectives
    -Configure the computers to use DHCP
    -Configure static addressing on the server
    -Use ipconfig to retrieve host IP information
    -Use ping to verify connectivity

<img width="555" height="318" alt="Screenshot 2026-10-18 191604" src="https://github.com/user-attachments/assets/d8ba21b7-f7a2-4353-83c1-378afe625f55" />

First things first we need to get these computers to use DHCP, so we don't have to assign address's ourselves. We can do this through the PC itself by clicking on it and navigating to the desktop section, there is where you'll find its IP configuration settings.

<img width="696" height="709" alt="Screenshot 2026-10-18 192424" src="https://github.com/user-attachments/assets/1a3eb498-278e-43d6-b304-2d965a4762f7" />

It might be an information overload for those who are just starting out but were essentially just clicking a button in the "IP Configuration" settings. As mentioned earlier DHCP is what were after right now, it stands for Dynamic Host Configuration Protocol its purpose is to automatically assign IP addresses in a network with a given range. It is in majority of networks ranging from enterprise to your home gateway. Click the button labeled "DHCP" and wait for a moment, you should see "DHCP request successful" and a new IP address automatically assigned. Do this same process with the other PC.

https://github.com/user-attachments/assets/78a8948c-f3e2-4a8a-965c-c449854f3d47

Now we need to actually test the connectivity between the two PC's, we can do this using the `ping` command. The `ping` command uses ICMP or Internet Control Message Protocol which is commonly used for troubleshooting networks. To successfully run it you need to insert the argument of whatever IP you are testing for example, `ping 172.12.1.2` is valid example (you can find the IP of a PC using `ipconfig` in the command line). After you have confirmed connectivity between the two PC's move on to the next step.

Servers are end point devices that are good with data typically hosting stuff like websites. So, in order to avoid confusion servers are assigned a static IP address. In order to do that we will need to click on "Server0" and go to the IP Configuration settings. If you want you could address it yourself but to save you some time, I will provide a valid configuration.

```
IP Address: 172.16.1.100

Subnet Mask: 255.255.255.0

Default Gateway: 172.16.1.254

DNS: 209.165.200.226
```

Confirm that Server0 is connected to the LAN (Local Area Network) use the `ping` command and make sure all packets are recieved.

This is the end of the lab.
