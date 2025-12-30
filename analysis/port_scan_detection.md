## Port Scan Detection

### Filter Used

tcp.flags.syn == 1 && tcp.flags.ack == 0


### Description
Port scanning generates multiple SYN packets without completing the TCP handshake, indicating reconnaissance activity.

### Observation
Sequential SYN packets targeting different ports were detected, indicating a port scanning attempt.
