
Shéma de la Topologie:*
```bash

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


 ```
### Tableau résumé
Hosts | `` |  `` |  `` | `` | ``
--- | --- | --- | --- | --- | ---
`server` | `192.168.56.20/24` | x | x | x | x
`imprimante` | x | `192.168.56.14/24` | x | x | x
`pro` | x | x | `192.168.56.12/24` | x | x
`RH` | x | x | x | `192.168.56.13/24` | x
`admin` | x | x | x | x | `192.168.56.11/24`

![Alt text](https://github.com/SilouanLC/monrepo/img/Capture.PNG"")
