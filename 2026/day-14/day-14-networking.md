## Quick Concepts (write 1–2 bullets each)
- OSI layers (L1–L7) vs TCP/IP stack (Link, Internet, Transport, Application)
    -> Open systems interconnection - (OSI) model is a ISO-developed conceptual framework from the 1980s that standardizes network communication into seven distinct layers. It enables diverse, incompatible systems to communicate,, assisting in troubleshooting, designing, and understanding network protocols.

    "Are pagli 

    1. Application -  Interfaces with end-user applications (e.g., browsers) using protocols like HTTP, FTP, SMTP.
    2. Presentation - Translates, encrypts, and formats data for the application layer.
    3. Session -  Manages sessions (connections) between applications, establishing, maintaining, and terminating them
    4. Transport - Handles end-to-end communication, flow control, and error correction (e.g., TCP, UDP).
    5. Network - Determines the best physical path for data, managing logical addressing (IP addresses) and routing.
    6. Data Link - Manages physical addressing (MAC addresses), node-to-node data transfer, and error detection from the physical layer.
    7. Physical -  Transmits raw bitstreams over physical mediums (cables, radio waves).  

    TCP/IP (Transmission Control Protocol/Internet Protocol) is the fundamental,4-layer suite of communication rules used to interconnect network devices on the internet and private networks. It breaks data into packets, manages transmission, routing, and ensures reliable delivery. TCP handles data organization/accuracy, while IP handles addressing and routing.

    1. Application Layer: Handles high-level protocols (HTTP, FTP, SMTP).
    2. Transport Layer: Uses TCP to establish connections and manage data flow.
    3. Internet Layer: Uses IP to address and route packets (e.g., IPv4/IPv6).
    4. Network Access Layer: Manages physical hardware connection

    TCP ensures reliability, like checking for errors and retransmitting lost packets.
    IP is connectionless, meaning it handles the routing of individual packets without establishing a constant connection

    The OSI model is a 7-layer theoretical framework for understanding network communication, while TCP/IP is a 4-layer practical model actually used for internet communication. TCP/IP is protocol-dependent and combines layers (Application, Network Access), whereas OSI is protocol-independent, providing a detailed, standardized reference for network functions. 

    Structure: OSI has 7 layers (Physical, Data Link, Network, Transport, Session, Presentation, Application). TCP/IP has 4 or 5 layers (Network Access, Internet, Transport, Application).
    Implementation: TCP/IP is used to build the internet, while OSI is primarily a teaching and reference tool.
    Approach: OSI uses a top-down approach developed before protocols; TCP/IP uses a bottom-up approach developed after protocols.
    Layer Mapping:  
        OSI (Session/Presentation/Application) = TCP/IP (Application).
        OSI (Network) = TCP/IP (Internet).
        OSI (Physical/Data Link) = TCP/IP (Network Access/Link).
    Reliability: TCP/IP is highly reliable; OSI is more general and theoretical. 



- Where **IP**, **TCP/UDP**, **HTTP/HTTPS**, **DNS** sit in the stack
- One real example: “`curl https://example.com` = App layer over TCP over IP”