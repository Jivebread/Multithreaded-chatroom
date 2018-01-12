# Multithreaded-chatroom
## Architecture of the program:
### Connection: 
#### When the server started:
Thread starts to accept connections from the clients
#### Client side when it starts connection:
###### Input: ip port number and username(which is limited to 16)
###### Server side: accept the connection add new user to the user list and broadcast the new user arrived.
Process When new connection arrives it gets added to the connection list and , that list is broadcasted amongst the existing users
It then gets hashed with the dictionary datatype variable hasha . Hasha hashes all the Ip address with the connection socket object.
	

#### When the clients send chats:
##### Client side: send a chat (if it’s more than 154 length it will not fit in the header format so not accepted)
##### Server side: thread reads the input and broadcast it to the users.

#### Every once in a while:
##### Server side : send everyone about the existing users.

##### When the clients leave the chats:
Client side: quit the chat by closing
Server side: Send every users about one users’ leaving
