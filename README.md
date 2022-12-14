# Net Practice

Created: July 30, 2022 11:14 AM
Tags: Network, School

> Project Status:  **accomplish**.
> 

---

Net-practice is a school project about networking, where we have to configure small-scale networks, the project has 10 levels, and every level is more complicated than the other, this project is a system Administration related exercise.

---

### **content:**

- **[Best Networking Resources](#best-networking-resources)**
- **[What is Networking?](#what-is-networking)**
- **[Types of networking](#types-of-networking)**
- **[What is TCP/IP?](#what-is-tcpip)**
- **[But What exactly is TCP/IP?](#but-what-is-exactly-is-tcpip)**
- **[IPv4 binary conversion](https://www.notion.so/Net-Practice-d62d9f9ad0994e9a8ad459476b143a43)**
- **[IPv6 binary conversion](https://www.notion.so/Net-Practice-d62d9f9ad0994e9a8ad459476b143a43)**
- **[What is a subnet Mask?](#what-is-a-subnet-mask)**
- **[Classes of IPv4 Addresses](#classes-of-ipv4-addresses)**
- **[subnetting is simple from Sunny](#subnetting-is-simple-from-sunny)**

---

### What is Networking?

- Networking enables devices to be connected to each other on a local area network (LAN) or to a larger network,  such as the internet.

### Types of networking:

- there are two types of networking: wired networking and wireless networking.
    - wired networking requires the use of a physical medium for transporting data.
    - wireless networking uses radio waves to transport data over the air without any cables.

### What is TCP/IP?

- TCP stands for Transmission Control Protocol
- IP stands for Internet Protocol

### But What exactly is TCP/IP?

- TCP/IP was built to help us to determine how a specific computer should be connected to the internet and how data should be transmitted between them, The purpose is to allow communication over large distances.
- An IP address is an identifier for a computer or a device on the network, every device has to have an IP address for communication purposes, An IP address consists of 2 parts: a network address and a host address, there are two versions of IP address IPv4 and IPv6:

---

### IPv4 binary conversion:

- IPv4: is the current version of the IP address, it has a 32-bit numeric address written as four numbers separated by dots called octets, the number range for every octet is from 0 to 255, this address version can produce over 4 billion unique addresses, computers and networks don???t read IP addresses in his standard numeric format, they only understand numbers in a binary format.
    - IPv4 binary conversion
        - Here is the 8-bit chart that we use to get a possible valid IP address
        
        | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
        | --- | --- | --- | --- | --- | --- | --- | --- |
        
        <aside>
        ???? for example, if we take a random IP address like:
        
        `134.2.101.245` his binary format is: 
        `10000110. 00000010. 01100101. 11110101`
        
        </aside>
        
        now how we did do this?
        
        - to convert the IP address we will take that string of numbers and start from left to right, for each value we see if we can subtract this value from the decimal remaining if we can???t, we put ???0??? under the binary value, if its the opposite And the answer is Yes we put ???1??? under the binary value.
        - We take IP address 134.2.101.245 to convert to binary we start with the first part ???134???
            - The Question: Can I subtract ???128??? from ???134??? ??? YES! so put ???1??? to 128
                
                ![1.png](utils/1.png)
                
            - The Question: Can I subtract ???64??? from ???6??? ??? NO! so put ???0??? to 64
                
                ![2.png](utils/2.png)
                
            - The Question: Can I subtract ???32??? from ???6??? ??? NO! so put ???0??? to 32
                
                ![3.png](utils/3.png)
                
            - The Question: Can I subtract ???16??? from ???6??? ??? NO! so put ???0??? to 16
                
                ![4.png](utils/4.png)
                
            - The Question: Can I subtract ???8??? from ???6??? ??? NO! so put ???0??? to 8
                
                ![5.png](utils/5.png)
                
            - The Question: Can I subtract ???4??? from ???6??? ??? Yes! so put ???1??? to 4
                
                ![6.png](utils/6.png)
                
            - The Question: Can I subtract ???2??? from ???2??? ??? NO! so put ???1??? to 2
                
                ![7.png](utils/7.png)
                
            - The Question: Can I subtract ???1??? from ???0??? ??? NO! so put ???.0??? to 1
                
                ![8.png](utils/8.png)
                
            - The first part of The IP address 134 is 10000110 in binary so we repeat the same way with the other parts of The IP address.
                - [Source for more Explanation](https://petri.com/csc_convert_ip_address_from_decimal_to_binary/)
    
    ---
    

### IPv6 binary conversion:

- IPv6: is the next generation of IP addresses, it has a 128-bit hexadecimal address, with
- this type of address IPv6 can produce over 340 undecillion addresses, it is made up of 8 sets of 16 bits, the 8 sets separated by a colon
    - IPv6 binary conversion
        - Here is the 4-bit chart that we use to get a possible valid IP address
            
            
            | 8 | 4 | 2 | 1 |
            | --- | --- | --- | --- |
            
            The possible character is from `0 to 9` and from `A to F`
            
            for example, if we take random IPv6 Addresses like:
            
            ---
            
            **`f145:4455:447e:fc46:06a0:a1d3:b03b:c24f`** 
            
            his binary would be :
            
            `1111000101000101 0100010001010101 0100010001111110 1111110001000110 0000011010100000 1010000111010011 1011000000111011 1100001001001111`
            
            ---
            
            now how we did do this?
            
            - first of all, we cannot use a double-digit number to represent 4 bits in hexadecimal, double-digit numbers are represented with a single alphabet (A-F), Each hexadecimal character represents 4 bits.
            - Now I can't break and convert all sets of this IP Address because of three things Version 6 of IP addresses is too long and  I'm lazy and finally their tons of websites and applications that can do that for us. but for knowledge, we gonna convert the first set only and you can repeat the same way with all other sets:
                - The first set is **`f145` so let's start with the first 4-bits,`f`** equal to $15$ in hexadecimal which means:
                    
                    ![a.png](utils/a.png)
                    
                    ~ so `**f**` is `1111`in binary
                    
                - Now let go to the second 4-bits, `**1` is $1$ in hexadecimal, which means xD:**
                    
                    ![b.png](utils/b.png)
                    
                    ~ so **`1`** is `0001` in binary
                    
                - Now let go to the 3rd 4-bits, **`4` is $4$ in hexadecimal, which means xD xD:**
                    
                    ![c.png](utils/c.png)
                    
                    ~ so **`4`** is `0100` in binary
                    
                - Now let go to the last 4-bits in this set, **`5` is $5$ in hexadecimal, which means -_-:**
                    
                    ![d.png](utils/d.png)
                    
                    ~ so **`5`** is `0101` in binary
                    
                - So the binary of the first set is all of them together `1111000101000101` now you can convert the other sets by yourself.
                    
                    ![https://www.gifcen.com/wp-content/uploads/2022/02/sleepy-gif-5.gif](https://www.gifcen.com/wp-content/uploads/2022/02/sleepy-gif-5.gif)
                    
                    - [A good tutorial about IPv4 and IPv6](https://www.youtube.com/watch?v=ThdO9beHhpA&ab_channel=PowerCertAnimatedVideos)
    
    ---
    
    ### What is a subnet Mask?
    
    - the subnet mask splits the IP address into the host or the network addresses, defining which part of the IP address belongs to the device and which one belongs to the network, the address ???255??? is always assigned to a broadcast address, and the address ???0??? is always assigned to the network address. Neither can be assigned to hosts, as they are reserved for these special purposes.
    
    ### What is Subnetting?
    
    - taking a network and dividing it into sub-networks, by accepting bits from the host part IP address  and using these bits to assign a number of smaller sub-networks
    
    ### What is a Switch?
    
    - switches are a device that connects multiple other devices or any networking device using ethernet, through a switch port, switches are usually found in larger networks
    - a network switch or switching hub is a device that receives incoming data packets and redirects them to their destination on a local area network
    
    ### What is the difference between switch and hub?
    
    - hub and switch are networking hardware that connects devices on a computer network to establish a LAN
    - the switch has a memory but the hub doesn't
    - the switch stores the MAC address table
        
        ![switch and hub.png](utils/switch_and_hub.png)
        
    
    ### Classful Address:
    
    - Classful addressing is a way to divide IPv4 Addresses into five groups named Class A, B, C, D, and E.
    - The Classful addressing was superseded by Classless addressing in order to reduce address depletion.
    
    ### Classes of IPv4 Addresses:
    
    - I recommend this video for you: **[Tricks to five classes of IPv4](https://www.youtube.com/watch?v=vcArZIAmnYQ&list=PLSNNzog5eydt_plAtt3k_LYuIXrAS4aDZ&index=1&t=4s&ab_channel=SunnyClassroom)**
    
    ![IPv4 Classes.png](utils/IPv4_Classes.png)
    
    ### subnetting is simple from Sunny:
    
    - full video [here](https://www.youtube.com/watch?v=ecCuyq-Wprc&list=PLSNNzog5eydt_plAtt3k_LYuIXrAS4aDZ&index=7&ab_channel=SunnyClassroom).
    
    ![subnetting is simple.png](utils/subnetting_is_simple.png)
    
    ---

    ### TIPS:
    
    - you can use  Packet Tracer Application to dive deep into networking like i did.
    - you can install it through Managed Software Center (MSC) if you???re a 42 or 1337 student or ask your local staff about it

    ---
    
    ### Best Networking Resources:
    
    - [Sunny Classroom: Full Playlist that covers all you need for this project and more.](https://www.youtube.com/playlist?list=PLSNNzog5eydt_plAtt3k_LYuIXrAS4aDZ)
    - [Tutorialspoint: Classful Vs Classless Addressing](https://www.tutorialspoint.com/classful-vs-classless-addressing#:~:text=Classful%20addressing%20is%20a%20technique,to%20reduce%20IP%20address%20depletion.)
    - [Packet Traveling - How Packets Move Through a Network](https://www.youtube.com/watch?v=rYodcvhh7b8&ab_channel=PracticalNetworking)
    - [How Data moves through the Internet - Networking Fundamentals](https://www.youtube.com/watch?v=YJGGYKAV4pA&ab_channel=PracticalNetworking)