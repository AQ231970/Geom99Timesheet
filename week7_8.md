**Creating a VM instance**
given you have an academic credit or have paid for credits:

1. this creates a first project on its own (if not, create one for making a vm instance)
2. ensure that at the top left side of the bar at your google cloud console, the right project is selected
3. in the hamburger menu on the left, under compute engine, select VM Instances
4. enable the compute engine API
5. roadblock i faced the first time: ensure the payment is set, especially if you are using credits requested on behalf of an institution or company, because it may ask you at step 4 to input payment information. In the context of the fleming requested credits, I had to ensure that under billing, the billing account was set to "Billing Account for Education"
6. once you have successfully enabled the API, select create instance
7. name your instance, keep defaults except the following
8. Update boot disk- odds are the default is a linux machine which in your case doesn't work because you have windows-> instead of public images, select custom images (if custom created by, say, Shawn or something). through this, you have access you Shawn's project as the source for images. Select relevant image and any other relevant configuration
9. If you want to use a web server on this instance, allow HTTP and HTTPS traffic under Firewall rules.
10. If you are happy with your vm instance settings, click create
11. This will take a few miutes -> it will copy the relevant image to your account and start the windows computer.
12. For the context of this assignment, we set up firewall rules: ingress direction of traffic, and allowed actions upon match, targetted all instances in the network, used an IPv4 range for which the range was originally set to the unrestricted 0.0.0.0/0. More ideal would be to use your computer IP, being that it is the most restrictive.
13. Specify the ports: in the context of the assignment, the TCP port is 444. But the default is 3389 for remote desktop protocol (RDP)
14. click create. Nwo your firewall rules have been created.
16. By navigating back to your vm instance (compute engine -> vm instances) you will see that your computer is running/started. You need to now create/determine the password for this vm. Clicke the little arrow next to RDP under "Connect".
18. Select "Set Windows Password"
19. In the context of the assignment, the username was set by Shawn to be "student". Select "SET". This will automatically generate a password for you to enter for your VM. SAVE THIS PASSWORD in a notepad file or something.
20. We do not use the internal IP, this would only be relevant inside the Google facility; it is always consistent. You can use the external IP— copy it.
21. Use your external IP to sign into Remote Desktop. In the start menu, navigate to Remote Desktop Connection -> paste the external IP as the computer. In the context of the assignment, we used a non-standard 444 TCP port, so we needed to specify that by following the external IP with ":444". If you use the standard TCP port 3389, there is no need for this.
22. Connect. This will prompt you for username and password. IF username is not prompted and a default is used, change this by selecting "Use a different account" under More Choices. You want to use the username (in this case, "student") that you used for the VM. Then enter the password that was generated (the one you copied into your notepad).
23. You might can a warning message about there not being any SSL certificate and the remote computer not being verified. Since we know that the computer is safe and we know why there is no certificate, we can accept it. If you are doing this in the future, ensure that you know exactly why there is no certificate or verification as well as the contents of the server.
24. IMPORTANT: The "x" does not turn off the remote desktop computer, nor does signing out. If you are done using the VM, you must navigate to the VM instances page, click the three dots, and select "STOP". This will prevent you from using excess credits and wasting money.

**SETTING UP A CONNECTION TO PUBLISH TO THE ARCGIS SERVER IN ARCGIS PRO**
1. Since the external IP changes every time you shut down and start you
