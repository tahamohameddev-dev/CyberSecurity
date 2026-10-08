---------------------------------------------

### Wireshark

- A network protocol analyzer
- It captures and shows network traffic in real time
- Used by network admins, security analysts, and developers
- Works on Windows, macOS, and Linux
- Download from: wireshark.org

#### Main Features

- **Packet Capture:** captures packets from a network interface
- **Protocol Analysis:** supports a huge number of protocols
- **Filtering:** shows only the traffic you care about
- **Visualization:** shows packets as headers and payloads

#### How to Run

1. Open Wireshark
2. Select a network interface
3. Click **Start** to begin capturing
4. Click **Stop** when you have enough data

---------------------------------------------

### Filters

- Filters narrow the captured data down to the packets you need
- There are too many packets every second, so filters are a must

#### Ports

```
tcp.port eq 25                    # port 25
tcp.port eq 25 or icmp            # port 25 or ICMP
tcp.port in {80, 443, 8080}       # several ports
port 80                           # port 80 (capture filter)
```

#### IP Addresses

```
host 192.168.1.1                  # from/to a specific host
ip.src == 192.168.1.1             # from a source
ip.dst == 192.168.1.1             # to a destination
net 192.168.1.0/24                # a whole subnet
ip.addr in {10.0.0.5 .. 10.0.0.9, 192.168.1.1..192.168.1.9}   # ranges
```

#### Combining Filters

- `and`, `or`, `not` : logical operators

```
host 192.168.1.1 and port 443
ip.addr == 192.168.1.1 and tcp.port == 443
ip.addr == 192.168.1.1 or ip.addr == 192.168.1.2
not icmp
ip.dst ne 224.1.2.3
```

#### Protocol / Content Filters

```
http                              # HTTP packets only
frame contains "password"         # packets containing a word
tcp.payload contains "pass"
tcp.flags.syn == 1                # SYN packets (TCP handshake)
http.request.method == "POST"     # POST requests only
http.request.method in {"HEAD", "GET"}
```

#### See Ready-Made Filters

- **Analyze → Display Filters...**
- Examples there: `not arp`, `ip`, `ipv6`, `tcp`, `udp`, `http`, `not arp and not dns`

---------------------------------------------

### Follow TCP Stream

- Rebuilds the full conversation between two devices

1. Right-click a packet from the stream
2. Select **Follow → TCP Stream**
3. A new window shows the whole conversation stitched together

- Shortcut: `Ctrl+Alt+Shift+T`
- Example from the course: an HTTP `GET / HTTP/1.1` request with `Host`, `User-Agent`, `Accept` headers

---------------------------------------------