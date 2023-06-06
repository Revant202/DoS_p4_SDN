# DoS attack, detection and prevention in SDN using p4
DoS attack detection and prevention
To run the DoS p4 program, follow these steps:
1.	Open the dos_p4_code folder in the terminal
2.	$ sudo p4run
3.	Mininet will open after the compilation is complete
4.	mininet> xterm h1 h2 s1
5.	In s1: $python get_digest.py
6.	In h2: $python receive.py 5000
7.	In h1:
a.	For performing DoS attack: $python dos.py 10.0.2.2 5000 1000
		(reciever will only recieve 100 packets, see s1 to get attacker IP)
b.	For sending packets at a normal rate: $python send.py 10.0.2.2 5000 1000
		(reciever will receive all the 1000 packets)

