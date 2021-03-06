 
<!--- the previous line with a space is needed for github pages
      the title is not needed here, as it is taken from the project description in Github 
--->

The SRv6 "micro segment" (uSID for short) solution is an extension to the SRv6 Network
Programming model. It allows expressing SRv6 segments with a very compact and 
efficient representation, for example using two bytes for uSID instead of using
a normal IPv6 address (16 bytes) for a regular SRv6 segment.

In the context of the [ROSE](https://netgroup.github.io/rose/) project, we have 
implemented the SRv6 uSID solution using the [P4](https://www.opennetworking.org/p4/) [language](https://github.com/p4lang/tutorials)
and realized a DEMO, illustrated in the following figure.

<!--- img source (new version in gslide):
      https://docs.google.com/presentation/d/1rV0ViQYk9lYUnJH16zvf5qBDUK4yTWAeHoryo6Fe0jo/edit#slide=id.g7f4100c2bd_6_0 
      export the slide as .png, cut to roughly 615x341, and upload in docs/images with the same name --->
![p4-srv6-usid-demo-topology.jpg](<./images/p4-srv6-usid-demo-topology.png>)

The demo runs on a mininet topology made up of eight P4 enabled switches (based on [bmv2](https://github.com/p4lang/behavioral-model) P4 software implementation) and two hosts that represent Site A and Site B. The source code and the detailed instruction to run the demo are reported below.

### P4 SRv6 uSID implementation source code and demo

[https://github.com/netgroup/p4-srv6-usid](https://github.com/netgroup/p4-srv6-usid)

### Reference IETF documents

"Network Programming extension: SRv6 uSID instruction" [Internet Draft](https://tools.ietf.org/html/draft-filsfils-spring-net-pgm-extension-srv6-usid)

"SRv6 Network Programming" [Internet Draft](https://tools.ietf.org/html/draft-ietf-spring-srv6-network-programming) 
              
"IPv6 Segment Routing Header (SRH)" [RFC 8754](https://www.rfc-editor.org/rfc/rfc8754.html)

### The P4 SRv6 uSID's Team

- Angelo Tulumello
- Stefano Salsano
- Marco Bonola
- Ahmed Abdelsalam
