# Troubleshooting
## isitthef5 game
1. Are we recieveing the traffic?
    1. DNS resolutuion
    2. Virtual server Connection stats
2. Are we delivering the traffic?
    1. Do we have a pool
        1. What is the pool status
    2. Are there Irules that impact load balancing decisions?
3. What modules are involved?
    1. LTM
        1. /var/log/ltm
    2. APM
        1. /var/log/apm
    3. ASM
        1. ASM - Event logs
4. Profile statistics
    1. TCP
        1. resets
    2. HTTP
        1. status codes
            1. 200 - success
            2. 300 - redirect
            3. 400 - Client Bad request
            4. 500 - Server Error processing request
    3. SSL 
        1. failed handshakes
        2. protocol version
            1. 1.0
            2. 1.1
            3. 1.2 
            4. 1.3
5. Logs
    1. Grep for virtual name
    2. Grep for iRule name
6. iRule logging
    1. Log 
        1. Headers
        2. status codes
        3. URI
        4. request body
        5. response body
7. TCPdumps
    1. capture interface or vlan
    2. clear text
8. SSLdumps
    1. askf5 SOLs
    2. keylog
