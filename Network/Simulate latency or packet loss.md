This can be achieved on Linux thand to the `tc` tool.

# Simulate complete packet loss

> sudo tc qdisc add dev eth0 root netem loss 100%

qdisc: _modify the scheduler (aka queuing_ _discipline)_  
add: _add a_ new _rule_  
dev eth0: _rules will be applied on device eth0_  
root: _modify the outbound traffic scheduler (aka known as the egress qdisc)_  
netem: _use the_ [_network emulator_](https://wiki.linuxfoundation.org/networking/netem) _to emulate a WAN property_  
loss: _the network property that is modified_  
100%: _introduce 100% packet loss_

# Reset network
> sudo tc qdisc del dev eth0 root

Source: https://netbeez.net/blog/how-to-use-the-linux-traffic-control/