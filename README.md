# VRCollaborativeWorkspace

SETUP GUIDE:
This system is intended for two windows computers with their own Occulus Rift and Leap motion. The two computers will be networked over an ethernet cable. From this point on the two computers will be referred to as Computer 1 and Computer 2.

On Computer 2:

(1) download all four assets

(2) create a new Unity file

(3) import all four assests

(4) Within the VR_CollaborativeWorkspace open the uniOSC_2 scene. (a) Click on the "Network Manager" in the Hierarchy tab, then look at the Inspector tab. (b) Under the "Network Manager (Script)" make sure the ClientID is "Client2", the Address is "C2" and the Server is "Server2". 

(5) Now we want to set up the correct IP Addresses: (a) Find the local hardware address for Computer 1. (b) Then back in Computer 2 go to UnityOSC-master/src/OSCHandler, and open the C# file. (c) in the function "public void init()" uncomment the two lines under C2 and comment the two lined under C1. (d) In CreateClient, change "10.2.128.58" to your local hardware address for Computer 1.

(6) Build the Project and Ensure VR is set up. Go to File/Build Settings: (a) click the "Add Open Scenes" button. (b) click the "Player Settings..." button on the bottom left and under XR Settings check the "Virtual Reality Supported" box. (c) finally click the "Build and Run"  Button.

On Computer 1:

(1) download all four assets

(2) create a new Unity file

(3) import all four assests

(4) Within the VR_CollaborativeWorkspace open the uniOSC_2 scene. (a) Click on the "Network Manager" in the Hierarchy tab, then look at the Inspector tab. (b) Under the "Network Manager (Script)" make sure the ClientID is "Client1", the Address is "C1" and the Server is "Server1". 

(5) Now we want to set up the correct IP Addresses: (a) Find the local hardware address for Computer 2. (b) Then back in Computer 1 go to UnityOSC-master/src/OSCHandler, and open the C# file. (c) in the function "public void init()" uncomment the two lines under C1 and comment the two lined under C2. (d) In CreateClient, change "10.2.128.58" to your local hardware address for Computer 2.

(6) Build the Project and Ensure VR is set up. Go to File/Build Settings: (a) click the "Add Open Scenes" button. (b) click the "Player Settings..." button on the bottom left and under XR Settings check the "Virtual Reality Supported" box. (c) finally click the "Build and Run"  Button.
