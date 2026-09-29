# Amazon EC2 — Virtual Machines, AMI, Instance Types & Sizes

---

## Virtual Machine & EC2 Introduction

### Amazon EC2 Kya Hai?

- **EC2 (Elastic Compute Cloud)** ek **tool/service** hai jo aapko **virtual server provide karta hai**.
- Simple works: **AWS ke bare server ke andar ek "chota apna server"** jisay **"virtual server" (instance)** kaha jata hai.

### EC2 Use?

- **Website host karna** ho ya koi bhi **activity perform karni ho**, aapka virtual server **doosre customers ke servers se independent** kaam karta hai.
- Matlab: **aap jo bhi apne virtual server par karte ho, uska doosre logon ke virtual servers par koi asar nahi parta** har instance **alag aur isolated** hota hai.



### Remote Login (SSH)

- Aap apne virtual server (EC2 instance) mein **SSH ke through remote login** kar sakte hain.
- Matlab: **apni asal machine se door baithe hue bhi**, aap us virtual server ko **control/access** kar sakte hain.



### Scaling & Template

- Jaise-jaise zaroorat barhti hai, **instances ki tadaad ko upar-neeche kiya ja sakta hai** (scaling).
- **Template** use hoti hai taake **naye instances ko jaldi aur consistent method se launch** kiya ja sake baar baar sab kuch manually set na karna pare.



### AMI (Amazon Machine Image)

- **Har instance alag hota hai** har ek ka apna **OS (operating system)** ho sakta hai.
- **AMI (Amazon Machine Image)** ek **"blueprint/template"** hoti hai jisse pata chalta hai ke **instance kis tarah ka hai** uska OS, software, aur configuration.
- Jab bhi **naya server launch karna** ho to **AMI se hi uska "record"/setup pata chalta hai** yani AMI batati hai ke us system mein **kya install hai aur wo kaisa configure hua hai**.
- **Website traffic aur code** bhi is setup ka hissa hote hain jo AMI ke through track/record hota hai.

> **Simple:** EC2 = virtual server milta hai | SSH = us server mein remote login | AMI = us server ka "blueprint/snapshot" jisse system ka pura record pata chalta hai

---



## EC2 Instance Launch & Instance Types



### AWS Kaise Manage Karta Hai?

-  **AWS poori tarah bara/mukammal server nahi deta** balke jab bhi zaroorat ho, **server ke andar se ek "instance" launch kiya jata hai**.
- Server launch karne ke liye **do cheezein zaroori hoti hain**:
  1. **AMI (Amazon Machine Image)** konsa OS/setup chahiye
  2. **Instance Type ki Family** konsi performance/resources chahiye



### Instance Type Family

- Aap **jaisa model run karna chahte ho, uske hisaab se sahi vCPU (virtual CPU) choose karna zaroori hai**.
- **Jaisa instance type choose karoge, wo waisa hi interface/performance provide karega**.

Types

### 1. General Purpose (Misal: T-series, M-series)

- **Balanced vCPU aur RAM** milti hai na zyada CPU-focused, na zyada RAM-focused.
- **Use:**
  - Websites
  - Development/testing
  - Chote (small) applications
  - General workloads (jahan koi khaas requirement na ho)



### 2. Compute Optimized (C-series)

- **Zyada CPU par focus** hota hai RAM zyada nahi milti, lekin **processing power zyada** hoti hai.
- **Use:**
  - High-performance computing (jaise batch processing)
  - Gaming servers
  - Scientific modeling
  - Media transcoding (video convert karna)



### 3. Memory Optimized (R-series)

- **Zyada RAM par focus** hota hai bara data **memory mein rakh kar fast process** karne ke liye.
- **Use:**
  - Bari databases
  - In-memory caching (jaise Redis)
  - Real-time big data processing
  - Wo applications jinhein **bohat zyada memory chahiye**



### 4. Storage Optimized (Misal: I-series, D-series)

- Us type ke liye jahan **zyada storage chahiye** hoti hai.
- *Misal:* Agar **60 hazaar videos** save/process karni hon, to **storage-heavy** setup chahiye hoga.
- **Use :**
  - Bari data warehousing
  - Distributed file systems
  - High-frequency database transactions



### 5. Accelerated Computing (Misal: P-series, G-series)

- Ye **specialized hardware jaise GPUs ya doosre accelerators** use karta hai matlab **"super-computer level" processing power**.
- **Use:**
  - Machine Learning
  - Graphics processing
  - Scientific computing

> **Simple:** General Purpose = balanced | Compute Optimized = CPU-heavy kaam | Memory Optimized = RAM-heavy kaam | Storage Optimized = zyada storage chahiye | Accelerated Computing = ML/graphics/GPU-heavy kaam

---



## Instance Size

- **AWS aapko different sizes deta hai** har instance type ke andar jese:
  - **t-type.small**
  - **t-type.medium**
  - **t-type.large**
  - **t-type.xlarge**
- **General rule:** Jitni **badi size** choose karoge, utne **zyada resources** (CPU, RAM) milenge.
- **Exact resources kya milenge** ye is baat par depend karta hai ke aapne **konsi Instance Family** choose ki hai (jese General Purpose, Compute Optimized, waghera).

> **Simple Example:** `t-type.small` = kam resources, chota kaam | `t-type.xlarge` = zyada resources, bara/heavy kaam

---



## Summary


| Concept                   | Simple                                                             |
| ------------------------- | ------------------------------------------------------------------ |
| **EC2**                   | Virtual server provide karne wala tool                             |
| **SSH**                   | Remote se apne virtual server mein login karna                     |
| **AMI**                   | Instance ka blueprint OS aur configuration ka record               |
| **Instance Launch**       | AMI + Instance Type Family dono chahiye                            |
| **General Purpose**       | Balanced websites, dev, small apps                                 |
| **Compute Optimized**     | CPU-heavy gaming, HPC, media processing                            |
| **Memory Optimized**      | RAM-heavy databases, caching, big data                             |
| **Storage Optimized**     | Storage-heavy file systems, data warehousing                       |
| **Accelerated Computing** | GPU/hardware-heavy ML, graphics, scientific computing              |
| **Instance Size**         | Small → Medium → Large → XLarge (jitni badi, utne zyada resources) |


