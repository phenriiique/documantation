---
layout: default
title: Graph
nav_order: 3
author: Pedro Henrique
---

<!-- - Begin: importing scripts -->
<!-- <script src="https://cdnjs.cloudflare.com/ajax/libs/mermaid/8.8.2/mermaid.min.js" integrity="sha512-x8NWYlEsC86ngfO24tbxW6pMuyn9gYnwEW0FcSobohDc3iLCXhmRkqYXgTfE7Jwy2YCTnHRfyum8LUIiyvmgWQ==" crossorigin="anonymous"></script> -->
<!--- End: importing scripts -->

<!-- IMPORT LAST VERSION https://www.jsdelivr.com/package/npm/mermaid -->
<!-- <script type="module">
import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@11.4.1/+esm'
</script> -->

## 1 Graph Example

#### Block Graph

<!-- %%{
  init: {
    'theme': 'base',
    'themeVariables': {
      'primaryColor': '#BB2528',
      'primaryTextColor': '#fff',
      'primaryBorderColor': '#7C0000',
      'lineColor': '#F8B229',
      'secondaryColor': '#006100',
      'tertiaryColor': '#fff'
    }
  }
}%% -->

```mermaid 
---
config:
  layout: fixed
---
flowchart TD
 subgraph s1["Internet - 0.0.0.0/0"]
        n1["Angola"]
        n2["Algar"]
  end
    n1 --> n3(["BDR"]) & n6["BRFW"]
    n2 --> n3
    n4["IX.br"] --> n3
    n3 --> n5["ext_transit"]
    n5 --> n8["NFTABLES"] & n7["BRFW"]
    n6 --> n9["Public_IP"]
    n7 --> n9
    n8 --> n9 & n10["ext_customers"]
    n10 --> n13["Lbaas - L4"] & n12["Lbaas - L7"] & n17["Border"]
    n13 --> n11["lbaas_tr"]
    n11 --> n12
    n12 --> n14["Untitled Node"]
    n14 --> n15["Untitled Node"]
    n15 --> n16["Untitled Node"]
    n17 --> n18["Untitled Node"] & n19["Untitled Node"]
    n9 --> n25["Border"]
    n21["DNS"] --> n23["DNS - Recurcivo"]
    n22["FRW"] --> n24["API"]
    n25 --> n20["MGC - Workload"] & n21 & n22
    n18 ~~~ n26["159.168.15.18<br>159.168.15.18<br>159.168.15.18<br>159.168.15.18"]
    n1@{ shape: rounded}
    n2@{ shape: rounded}
    n6@{ shape: rounded}
    n4@{ shape: rounded}
    n5@{ shape: rounded}
    n8@{ shape: rounded}
    n7@{ shape: rounded}
    n9@{ shape: rounded}
    n10@{ shape: rounded}
    n13@{ shape: rounded}
    n12@{ shape: rounded}
    n11@{ shape: rounded}
    n18@{ shape: rect}
    n26@{ shape: text}
    style n1 stroke:#BBDEFB,fill:#BBDEFB
    style n2 fill:#BBDEFB
    style n4 fill:#BBDEFB
    style s1 fill:#C8E6C9
```


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



```mermaid
---
config:
  layout: fixed
---
flowchart TD
 subgraph s1["Internet - 0.0.0.0/0"]
        n1["Angola"]
        n2["Algar"]
  end
    n1 --> n3(["BDR"]) & n6["BRFW"]
    n2 --> n3
    n4["IX.br"] --> n3
    n3 --> n5["ext_transit"]
    n5 --> n8["NFTABLES"] & n7["BRFW"]
    n6 --> n9["Public_IP"]
    n7 --> n9
    n8 --> n9
    n8 --> n10["ext_customers"]
    n1@{ shape: rounded}
    n2@{ shape: rounded}
    n6@{ shape: rounded}
    n4@{ shape: rounded}
    n5@{ shape: rounded}
    n8@{ shape: rounded}
    n7@{ shape: rounded}
    n9@{ shape: rounded}
    n10@{ shape: rounded}
    style n1 stroke:#BBDEFB,fill:#BBDEFB
    style n2 fill:#BBDEFB
    style n4 fill:#BBDEFB
    style s1 fill:#C8E6C9
```