---
layout: default
title: Mermaid Examples
nav_order: 3
author: Pedro Henrique
---

<!-- - Begin: importing scripts -->
<!-- <script src="https://cdnjs.cloudflare.com/ajax/libs/mermaid/8.8.2/mermaid.min.js" integrity="sha512-x8NWYlEsC86ngfO24tbxW6pMuyn9gYnwEW0FcSobohDc3iLCXhmRkqYXgTfE7Jwy2YCTnHRfyum8LUIiyvmgWQ==" crossorigin="anonymous"></script> -->
<!--- End: importing scripts -->

<!-- IMPORT LAST VERSION https://www.jsdelivr.com/package/npm/mermaid -->
<script type="module">
import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@11.4.1/+esm'
</script>

## 1 Mermaid Example

#### Block Graph


<div class="mermaid">

block-beta
      columns 15
        space:5
        ix:5
        space:5

        block:row2("Internet - 0.0.0.0/0"):15
            internet1
            space
            internet2
        end

        space:6
        bdr:3
        space:6

        space:3
        ext_transit:8
        space:4

        bfw1:2
        space
        bfw2:2
        space
        nftables:5
        space:4

        space:12
        lbass_l4:2
        space
        public_ip:5
        space
        ext_customers:5
        space
        ne1_lbaas_rt:2
        space

        space:12
        lbass_l7:2
        space

        border1:5
        space
        border2:5
        space
        ne1_swift:2
        space
        
        fwr:1
        space
        dns
        space
        mgc
        space
        mgc_pprod:2
        space
        mgc_prod:2
        space
        berder3:2


ix --- bdr
internet1 --- bdr
internet2 ---bdr
bdr --- ext_transit
ext_transit --- nftables
ext_transit --- bfw2
internet1 --- bfw1
bfw1 --- public_ip
bfw2 --- public_ip
public_ip --- border1
border1 --- fwr
border1 --- dns
border1 --- mgc        
</div>



#### Relationship Flow

```mermaid
graph TD;
    A(ClassA) --- |Extends| B(ClassB);
    C(ClassC) --- |Extends| D(ClassD);
    E(ClassE) --- |Extends| B;
    F(ClassF) --- |Extends| D;
    G(ClassG) --- |Extends| D;
    B --- |Extends| D;
```
