Files in the directory:

	1. pg1lib.py
 	    It contains some helper functions that help us establish communication between the server and the client.
		1. getPubKey()		Get the public key of server/client's.
		2. encrypt(message, pubkey)	Encrypt the message with a public key.
		3. decrypt(cipher)		Decrypt the message by a private key.
		4. checksum(data)		Check the sum of the message received.
	2. udpserver.py
	    It contains two functions that start the server and receive messages from the client.
	3. udpclient.py
	    It contains two functions that send messages to the server.

To run/test the code:

	1. Change the hostname and port in "udpserver.py" and "udpclient.py" to your own hostname and port, and save your change.
	2. Send all of these three files from local to remote using the command "scp (local address) (remote address)"
		After that, run“ls”to see if these files have been uploaded successfully.
	    eg.  scp ./Desktop/IS496/udpserver.py zemingg2@student00.ischool.illinois.edu
 	3. Connect to two different student machines in two terminal windows with the command "ssh (remote address)"
		Determine which terminal is the server and which terminal is the client.
	   eg.  ssh zemingg2@student00.ischool.illinois.edu
	          ssh zemingg2@student01.ischool.illinois.edu
	4. In the server command line window, type "python3 udpserver.py [port]"
	   eg.  python3 udpserver.py 41002
	5. In the server command line window, type "python3 udpclient.py [hostname] [port] [test message]"
		Notice to not compile the client file in the server window!
	   eg.  python3.udpclient,py student00.ischool.illinois.edu 41002 "Hello World!"
