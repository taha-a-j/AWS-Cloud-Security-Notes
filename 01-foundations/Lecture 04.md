# AWS Cloud Practitioner — Domain 1 & 2

---

## Cloud Migration: The 6 R's

**Migration** ka matlab hai: **apne existing systems ko apne data center se nikaal kar cloud mein shift karna**.

AWS har application ko cloud par move karne ke liye **6 common strategies** batata hai inhein **"6 R's"** kehte hain. Har ek is baat ka **alag method** hai ke **application ko kaise move kiya jaye**.


| Strategy                                  | Simple Words                                                                                                                                           |
| ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **1. Rehost** ("Lift and Shift")          | App ko **jaisa hai waisa hi** cloud par move kar dena **koi change nahi**. Ye **sabse tez aur sabse simple** method hai.                               |
| **2. Replatform** ("Lift, Tinker, Shift") | App ko move karte waqt **chhoti-chhoti improvements** kar dena, lekin **koi bara redesign nahi** karna.                                                |
| **3. Repurchase**                         | **Purani app ko chhor kar** ek **naya (aksar SaaS) product** use karna.                                                                                |
| **4. Refactor / Re-architect**            | App ko **bari major changes ke sath dobara banana**, taake cloud ke features **poori tarah use** ho sakein. Ye **sabse zyada effort** wala method hai. |
| **5. Retire**                             | Realize karna ke **ab is app ki zaroorat hi nahi** is liye **shut down** kar dena.                                                                     |
| **6. Retain**                             | App ko **abhi ke liye wahin rehne dena** **move na karna**, apne server par hi rakhna.                                                                 |


> **Method:** Rehost = jaisa hai waisa move | Replatform = thori si improvement | Repurchase = naya product | Refactor = poori tarah rebuild | Retire = band kar do | Retain = abhi mat hilao

---



## The Shared Responsibility Model (Introduction)



### Plain Meaning

Cloud mein **security ek "team job" hai** jo **AWS aur aap dono ke darmiyan share** hoti hai. **AWS kuch cheezon ki security karta hai**, aur **aap baaki cheezon ki**. Koi bhi ek party **sab kuch nahi karti**.

### **Security OF the Cloud**

AWS **in cheezon ka malik hai aur inhein chalata hai**:

- **Physical buildings** (data centers)
- **Hardware**
- **Global network**
- **Basic software** jo cloud ko chalata hai

> Ye cheezein **aap kabhi touch nahi karte** **AWS inko protect karta hai**.



### **Security IN the Cloud**

Aapki zimmedari mein ye cheezein aati hain:

- **Aapka data**
- **Access** **kis ko kya access diya jaye**
- **Aapka password**
- **Settings/configuration**
- **Identity & Access management**
- **Firewall**
- **Application-level security**
- **Patches** (software update karna)

---



## How Responsibility Shifts

 **AWS aur aapke darmiyan** Responsibility **ki line** is baat par depend karti hai ke **aap konsi service use kar rahe hain**. **Jitna zyada AWS manage karega, utni kam** Responsibility **aapki hogi**.


| Service        | Type                  | Our's Management                   | AWS's Management                |
| -------------- | --------------------- | ---------------------------------- | ------------------------------- |
| **Amazon EC2** | IaaS (virtual server) | OS, patching, firewall, apps, data | Hardware, hypervisor, facility  |
| **Amazon RDS** | Managed database      | Aapka data, access, kuch settings  | OS, database patching, hardware |
| **AWS Lambda** | Serverless            | Sirf aapka code aur permissions    | OS, servers, scaling, patching  |




### Pattern

> **EC2** = aap **sabse zyada manage** karte ho (ye ek raw/basic server hi hota hai).
> **RDS** = **AWS database ka admin/patching sambhal leta hai**, is liye aap **kam manage** karte ho.
> **Lambda** = **AWS almost sab kuch manage karta hai** aap sirf apna **code aur uski permissions** dekhte ho.
>
> **Zyada managed service = aapki kam zimmedari.**

---



## IAM (Identity and Access Management)

**IAM** ka matlab hai: **company mein har kisi ki identity aur access ko manage karna** bilkul **HR department** ki tarah, jo check karta hai ke **kaun kaun hai aur kis ko kya access milega**.

- Jab koi **login karna chahta hai**, to uski **identity check ki jati hai** is ke liye **password** use hota hai.



### Two Important Words

1. **Authentication** — **Proving who you are**
  - Matlab: **password, username** etc se prove karna ke **aap wahi ho jo aap keh rahe ho**.
2. **Authorization** — **"Passport" jaisa concept**
  - Matlab: **aap kya karne ki ijazat rakhte ho** For Example, agar **kisi cheez ko delete karne ki permission di gayi ho to hi** wo delete kar sakega.

> **Example:** **Boarding pass** ye check karta hai ke aap **flight/seat** tak access rakhte ho ya nahi (Authorization), jabke **passport** ye prove karta hai ke **aap kaun ho** (Authentication).

---



## IAM Building Blocks — Users, Groups, Roles, Policies

IAM **4 pieces** par consist hai:

### 1. IAM User

- Ek **user = ek identity, ek insaan (ya ek application) ke liye** uska **apna login** hota hai.
- *Example:* Kisi employee **"Sara"** ke naam ka IAM user.



### 2. IAM Group

- Ek **group = un users ka "bucket"** jinhein **same permissions** chahiye hoti hain.
- Aap **users ko group mein daaltay ho, group ko permissions dete ho**, aur **group ke andar ka har user wo permissions le leta hai**.
- Ye **ek-ek karke permission set karne se zyada asaan** hai.
- *Example:* Ek **"Developers"** naam ka group.



### 3. IAM Role

- Ek **role = permissions ka aik set** jo **temporarily** kisi **user, application, ya AWS service** ke through "**pehna (worn)**" ja sakta hai ye **hamesha ke liye kisi ek insaan se bandha nahi hota**.
- Roles **temporary credentials** use karte hain.
- *Example:* Ek **EC2 server** kisi **"role assume"** karta hai taake wo **storage bucket read** kar sake **bina password store kiye**.



### 4. IAM Policies

- Policy ek **document** hoti hai jo **batati hai ke kya allowed hai aur kya nahi** ye **Users, Groups, ya Roles** ke sath attach ki jati hai.

---



## Summary


| Concept                          | Simple Works                                             |
| -------------------------------- | -------------------------------------------------------- |
| **Cloud Migration**              | Apne data center se cloud mein systems move karna        |
| **6 R's**                        | Rehost, Replatform, Repurchase, Refactor, Retire, Retain |
| **Shared Responsibility Model**  | Security AWS aur aap ke darmiyan divide hoti hai         |
| **AWS: "Security OF the Cloud"** | Physical buildings, hardware, global network             |
| **Aap: "Security IN the Cloud"** | Data, access, password, config, firewall, patches        |
| **EC2 / RDS / Lambda**           | Zyada managed service = kam Responsibility aapki         |
| **Authentication**               | Aap kaun ho prove karna (password/username)              |
| **Authorization**                | Aap kya karne ki ijazat rakhte ho                        |
| **IAM User**                     | Ek insaan/app ki ek identity                             |
| **IAM Group**                    | Same permissions wale users ka bucket                    |
| **IAM Role**                     | Temporary permissions, kisi ek insaan se bandhay nahi    |
| **IAM Policy**                   | Document jo permissions define karta hai                 |


