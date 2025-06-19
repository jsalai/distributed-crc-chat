# distributed-crc-chat
In this assignment, you will develop a P2P chat application loosely based on the IRC protocol. Your task is to implement the functionalities as described in the docstrings of each class and method in ChatServer.py files. After implementation, your code will be submitted to Gradescope for automated testing.

Objectives
Implement a chat server (CRCServer class in ChatServer.py).
Ensure your implementation adheres to the specifications in the provided docstrings.
Pass all automated tests on Gradescope.
Files
ChatServer.py: Contains the CRCServer class with methods that need to be implemented.
ChatClient.py: Contains the CRCClient class with methods that need to be implemented. You do not need to implement anything in this file.
ChatMessageParser.py: Contains a helper class to parse CRC messages. You do not need to implement anything in this file.
CRCTestManager.py: Responsible for running the various tests examining your code's performance
.vscode\launch.json: A configuration file for a VS Code project that simplifies testing your application by running both client and server simultaneously in different terminals. This configuration file will only work in VS Code.
Instructions
Download Template Files: Begin by downloading the provided zip file and extracting it to a folder on your computer. Open this folder in VS Code (or an equivalent IDE).

Implement the CRCServer Class (ChatServer.py):

Complete the __init__ method.
Implement the setup_server_socket method to set up the server socket an register with the selector.
Implement the connect_to_server method to connect to a remote CRC server on startup.
Implement the check_IO_devices_for_messages method to manage the main loop responsible for processing input and output via the selector.
Implement the cleanup method to release all allocated resources on shutdown.
Implement the accept_new_connection method to handle new connection requests from other servers and clients.
Implement the handle_io_device_events method to handle read and write events from connected sockets
Implement the handle_messages method to direct received messages to the appropriate handling function.
Implement the send_message_to_host method to send a message to a specific host based on ID.
Implement the broadcast_message_to_servers method to broadcast a message to the entire network of connected machines.
Implement the broadcast_message_to_adjacent_clients method to broadcast a message to the adjacent clients.
Implement the send_message_to_unknown_io_device method to to send a message to a device based on an io_device value (from select) rather than based on ID.
Implement the handle_server_registration_message method to handle a server registration message.
Implement the handle_client_registration_message method to handle a client registration message.
Implement the handle_status_message method to handle a status update message.
Implement the handle_client_chat_message method to handle a chat message from a client.
Implement the handle_client_quit_message method to handle a quit message from a client.
Testing Your Code Locally:

Before submitting, test your implementation locally. I've provided two files stored in the source directory to use for your testing. Successfully copied files should be saved to the received_files folder.
Ensure that your classes and methods work as expected according to the specifications in the docstrings.
Submission to Gradescope:

Once you have completed the implementation, submit ChatServer.py to Gradescope.
Your submission will be automatically tested against a suite of unit tests.
Your code must pass all tests in order to receive credit for this assignment.
Notes
Pay close attention to the details in the docstrings, as they describe the required functionality.
Ensure that your code handles exceptions and edge cases as described.
Comment your code where necessary for clarity.
Remember to follow good coding practices.
