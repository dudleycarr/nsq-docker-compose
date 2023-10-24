# Notes

### Why is each nsqd configured with a unique TCP and HTTP port?

The configuration exposes the TCP and the HTTP port for each nsqd instance to the host machine.
The exposes ports have to be unique. When the configured TCP and HTTP ports of the
service match the Docker exposed ports, nsqadmin nsqd nodes view showing TCP and HTTP ports will
be correct from the host machine perspective.

### Should I run multiple nsqd instances on the same host?

No. This configuration is for simulating interacting with multiple nsqds on your own machine.
