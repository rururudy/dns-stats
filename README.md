# dns-stats
CLI tool for showing bind/named stats. like iostat but for DNS.

named process was using a bunch of CPU, so I wanted a rough estimate
of the number of queries per second.  The accuracy of the output is
not important (with a sample period of 1 second, I expect some odd,
artificial fluctuations when the timestamp looks like 2 seconds when it is
really 1.0001 seconds)

## Usage: perl dns-stats 
Here is an example of the output:
  938 QUERY/s ,   938/s in,   149/s out, 67% Fast 25% OK  6% Slow, 8.0% IPv6
 1847 QUERY/s ,  1847/s in,   315/s out, 48% Fast 40% OK 10% Slow, 8.2% IPv6
 1557 QUERY/s ,  1557/s in,   264/s out, 57% Fast 33% OK  8% Slow, 9.8% IPv6
 1211 QUERY/s ,  1211/s in,   193/s out, 54% Fast 31% OK 13% Slow, 8.4% IPv6
 1168 QUERY/s ,  1168/s in,   194/s out, 64% Fast 23% OK 12% Slow, 7.6% IPv6


