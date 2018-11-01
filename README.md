# Scaling the Root system by managing multiple root zones

From the practice of Yeti DNS, it is found that scaling the Root server system by adding more name servers in existing Root zone only results a large response (beyond 1500 octets). It is a dead end given the IP fragmentation is still a problem in both IPv4 and IPv6 (more serious).

However, the approach building a Root server testbed described in RFC8483 actually enabled people to build and operate their own root server system in their countries or regions. They are usually referred as to alternative root, another words, “illegal” Root Server system. However, uncoordinated alternative Root server systems introduces the risk of different name spaces by arbitrarily editing the content of root zone for commercial purpose or political purpose. It will end up with a Internet Fragmentation [WEF report] with different Intranets. The value of current modern Internet based on one unique Internet Identifier will be largely ruined. No one benefits from this.

Actually it is not the fault of RFC8483 and related technical activities. People in ICANN scope spent nontrivial effort on technical requirement and governance model of Root server operator in [RSSAC024](https://www.icann.org/en/system/files/files/rssac-024-04nov16-en.pdf) and [RSSAC037](https://www.icann.org/en/system/files/files/rssac-037-15jun18-en.pdf). But no effort was put on discussion and experiment on scaling the Root server system with potential technical approaches. 

It is ICANN's key responsibility to keep a unique Internet identifier with more open heart for positive approaches and efforts. One experience ICANN can borrow from Yeti DNS is that the root system can scale in a way with multiple versions of root zone operated by different root zone maintainers (more than one VeriSign's role). In each version of root zone, different set of root servers (13 Root servers in each set) can function well in parallel instead of relying on one set of root server with 13 limitation. In the aspect of DNSSEC, IANA KSK can be shared among different root zone. ZSK can be different and operated by different root zone maintainers. PTI/IANA can sign different DNSKEY sets. And root zone maintainers can sign separately and publish the root zone as VeriSign does. So the DNSSEC deployed in Root works fine and the name space in top level, signed non-apex data in root zone is kept intact as well. 

As to the root zone maintainers, the Regional Internet Registries (RIRs) or some large countries are potential candidates for this job. It is technical feasible, and of much political sense to create more than one regional root zones for different regions in the world. In each region, capable and responsible root server operators can be chosen and regional root server maintainers will serve a better role to coordinate this task other than ICANN, in which the accountability responsibility will be taken among different entities other than ICANN/PTI as well. 






