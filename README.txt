                                                                          TCP VS UDP CLIENT-SERVER COMPARISON

                                                                                  RUNNING THE PROGRAMS

1. First we run TCP Client Server by opening a terminal and then running python tcp_server.py. This will start the server.

2. Now we open a new terminal to run the TCP client (python tcp_client.py), the client will send 100 messages to server and receive responses. RTT will be logged in tcp_log.txt.

3. We run the UDP server by opening a new terminal (python udp_server.py).

4. We run the UDP client now on another terminal (python udp_client.py), the client will again send 100 messages to the server, results logged in udp_log.txt.


                                                                                   Expected Outputs

1, With TCP all 100 messages will be received.
2, With UDP about 20% of the messages will be lost, so about 80 messages should be received.
- The terminal will display message exchanges between client and server.
 
                                                                              RECORDED TERMINAL OUTPUTS

Example TCP Log Output (tcp_log.txt):
Sent: Message 1, RTT: 0.012115 sec
Sent: Message 2, RTT: 0.011263 sec
Sent: Message 3, RTT: 0.011425 sec
Sent: Message 100, RTT: 0.009876 sec

Example UDP Log Output (udp_log.txt):
Sent: Message 1, RTT: 0.005618 sec
Sent: Message 2, RTT: 0.004462 sec
Lost: Message 4
Total packets lost: 19/100

                                                                                    OBSERVATIONS

1️ Latency Comparison
TCP naturally has higher latency because it waits for acknowledgements and retransmission, while UDP has lower latency because it does not wait for acknowledgements.

2️ RELIABILITY
TCP ensures reliable delivery of packets and also has retransmission for dropped packets, however packets can be dropped when using UDP.

3️ THROUGHPUT ANALYSIS
UDP is unreliable but fast, while TCP is slower because of acknowledgements.

4️ USE CASES
TCP is used in HTTP, file transfers, emails while UDP is used for VoIP, video streaming, online gaming.

                                                                                   RESOURCES USED

Youtube and online resources for socket programming guides.
Wikipedia for information on use cases, observation etc.

