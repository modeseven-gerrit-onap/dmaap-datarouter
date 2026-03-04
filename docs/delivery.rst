.. This work is licensed under a Creative Commons Attribution 4.0 International License.
.. http://creativecommons.org/licenses/by/4.0

Delivery
==============

Below is a diagram of the DMaaP Data Router project docker containers and the connections between them.

.. mermaid::

   graph TD
       MARIADB --> DR-PROV
       DR-PROV --> DR-NODE

       subgraph "dr-prov Container"
           DR-PROV
       end

       subgraph "dr-node Container"
           DR-NODE
       end

       subgraph "MariaDb Container"
           MARIADB
       end

       classDef blue fill:#33f,stroke:#333,color:#fff
       classDef yellow fill:#ff0,stroke:#333,color:#000
       classDef orange fill:#f90,stroke:#333,color:#000

       class DR-PROV blue
       class DR-NODE yellow
       class MARIADB orange
