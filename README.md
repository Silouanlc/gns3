
Shéma de la Topologie:

                                                                 192.168.56.10
                                                                +------------------+
                                  +-----------+                 |                  |
                                  |           |                 |                  |
                                  |    NAT    +-----------------+     Pfsense      |
                                  |           |                 |                  |
                                  +-----------+                 |                  |
                                                                +--------+---------+
                                                                         |
                                                                         |
                                                                   Trunk |
                                                                         |
                                                                         |
192.168.56.20                                                            |                                192.168.56.11
   +--------+                 +-----------------+                +-------+---------+                     +--------+
   | Serveur|     Vlan 50     |                 |     Trunk      |                 |       Vlan 10       | Admin  |
   |        +-----------------+     Switch      +----------------+     Switch      +---------------------+        |
   |        |                 |                 |                |                 |                     |        |
   +--------+                 +-----------------+                +-------+---------+                     +--------+
                                                                         |
                                                                         |
                                                                         |
                                                                   Trunk |
                                                                         |
                                                                         |
                                                                         |
                                                                 +-------+---------+    Vlan 20     192.168.56.12
                                                                 |                 |               +---------+
                                                                 |     Switch      +---------------+         |
                                                                 |                 |               |   Pro   |
                                                                 +-+-------------+-+               |         |
                                                                   |             |                 +---------+
                                                                   |             |
                                                          vlan 40  |             |  Vlan 30
                                                                   |             |
                                                                   |             |
                                                                   |             |
                                                              +----+----+    +---+----+
                                                              |         |    |        |
                                                              Imprimante|    |   RH   |
                                                              |         |    |        |
                                                              +---------+    +--------+
                                                            192.168.56.14    192.168.56.13


