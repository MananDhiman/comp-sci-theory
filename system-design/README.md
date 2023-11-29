# System design

## [NeetCode](https://www.youtube.com/watch?v=i53Gi_K3o7I)

**Vertical scaling**: adding h/w to single system

**Horizontal:** adding new servers (complicated, one may take all load)

**CDN:** for static files (img, video, html/css) No app logic, and just files

**Caching:** storing data to fetch it faster

we use load balancer (may also be routed to nearest location)

**Networking:** Files broken down into individual packets and sent using TCP / ICP protocol.

- TCP: ensures all packets sent. low level. keeps sending until data sent
- UDP: no acknowledgement, live streaming, video call
- HTTP (Application layer protocol): used on daily basis. client server model. **Contains:** Request header (where,from,metadata), body (package contents)

**Api patterns:**

- REST stateless
- GraphQL (by FB in 2015): instead of multiple queries, make single req. and choose which resources to fetch
- grpc: (considered a framework. by google in 2016) server to server communication serialised into binary so efficient to store

**web sockets:** chat apps
db are acid compliant: durability, isolation (concurrent transactions), atomicity: all trans. are all or nothing, consistency: foreign key

**Sharding:** if no foreign keys, then split db into multiple, and scale horizontally.

**shard key:** Which data on which machine? sharding is complicated so we create read only copies of data. leader (original source), follower is copy

**Message Queue**: if data input greater than storage speed then use message queue to temporarily hold data
