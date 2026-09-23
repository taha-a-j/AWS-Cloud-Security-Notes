# Cloud Service Models & Cloud Economics

---

## Cloud Service Models

### 1. Infrastructure as a Service (IaaS)

- Yahan AWS **laptop, servers** waghera **deta hai** jinko **control/manage** karna user (customer) ka kaam hota hai.
- AWS sirf **infrastructure ki responsibility** leta hai matlab **khud** (customer) ko sab kuch **manage karna parta hai**: **OS, code, hosting, error fixing** normal setting bhi **user ko khud karni parti hai**.
- **Sabse zyada control**, lekin **sabse zyada responsibility** bhi user par hoti hai.
- *Misal:* Amazon EC2

### 2. Platform as a Service (PaaS)

- Aap sirf **code likho, website banao** **baaki sab kuch AWS khud handle kar leta hai**.
- **AWS** khayal rakhta hai: **error handling, operating system, hosting** sab kuch AWS **secure way mein** manage karta hai.
- Server mein **"bas code dena hai aur pay karna hai"** baki ki tension nahi.
- **AWS khud b sab kuch manage kar sakta hai** user ko underlying infrastructure se matlab nahi rehta.
- *Misal:* AWS Elastic Beanstalk



### 3. Software as a Service (SaaS)

- Yahan **code likhne ki zaroorat hi nahi hoti** ye ek **ready-made website/app type** hoti hai.
- Features pehle se bani hui website milti hai **hosting, OS "sab kuch already ready hota hai bas user ko use karna hota hai"**.
- Yahan **sab kuch AWS (ya provider) par depend karta hai** **Database, OS, error handling, network, setup, machine** sab kuch provider khud manage karta hai.
- *Misal:* Gmail, Netflix, Dropbox

> **Yaad rakhne ka tareeqa:** IaaS mein zyada control, kam ease. SaaS mein kam control, zyada ease. PaaS beech mein hai.

---



## Cloud Economics (Paison Terms)



### 1. CapEx — Capital Expenditure

- **Misal:** Software banane ke liye **building khareedni pare** (ya server room banana pare) ye ek **bara, one-time kharcha** hota hai.
- Jab bhi koi **cheez (hardware/physical asset)** use karni ho, pehle **pay karna parta hai, tab use kar sakte hain**.
- **CapEx = kisi physical cheez ki bari, one-time purchase**, jo aap **istemaal karne se pehle** pay karte hain.
- **Misal:** apne servers khareedna, apni building khareedna.



### 2. OpEx — Operational Expenditure

- Jitna **use karo**, **utna hi pay karo** ye "**running things ka cost**" hai.
- **Chhote, ongoing (musalsal) kharche** hote hain jo cheezein chalane ke liye lagte hain.
- Aapka **monthly AWS bill OpEx hai** aap **jitna use karte ho utna pay karte ho**.
- **Cloud Benefits:** bara CapEx ko **flexible OpEx mein badal deta hai** matlab bara upfront kharcha nahi karna parta.



### 3. TCO — Total Cost of Ownership

- **TCO = kisi cheez ka asal, poora kharcha** jisme **saare chupey huay (hidden) kharche bhi shamil hain**.
- Apne server room ka TCO sirf server ki qeemat nahi hota is mein shamil hai:
  - **3 servers khareedna**
  - **Engineers** (unko maintain karne wale)
  - **Security guard**
  - **AC (cooling)**
  - **Bijli aur paani (electricity/water)**
- **AWS ka model: "Pay as you go"** jitna use karo, utna hi pay karo, koi hidden extra kharcha nahi.



### Exam Tip (Important)

> Exam mein aksar aisa poocha jata hai: kisi company ka problem describe karke poochte hain **kaunsa benefit us problem ko solve karta hai**.
>
> **Misal:** *"Company bari upfront hardware purchase se bachna chahti hai"* → Iska matlab hai: **CapEx ko variable expense (OpEx) se trade karna** — yani bara ek-waqti kharcha karne ki bajaye, chhote-chhote ongoing kharche karna.

---



## Benefits of AWS

1. **Trade Capital Expense for Variable Expense**
  Bari hardware khareedne ki bajaye, sirf utna hi pay karo jitna use karo (CapEx → OpEx).
2. **Benefit from Massive Economies of Scale**
  Kyunke AWS lakhon customers ke liye resources use karta hai, is liye cost kaafi kam ho jati hai jo saving customers tak pohanchti hai.
3. **Stop Guessing Capacity**
  Pehle companies ko guess karna parta tha ke kitna server chahiye hoga agar kam guess kiya to problem, zyada guess kiya to paisa waste. **Cloud mein zaroorat ke hisaab se resources scale (up/down) kar sakte ho.**
4. **Increase Speed and Agility**
  Naye resources (server, database) **minutes mein** mil jate hain pehle hardware order karne mein hafte/mahine lagte the.
5. **Stop Spending Money on Running and Maintaining Data Centers**
  Apna data center chalane ki bajaye, AWS ye kaam khud karta hai company apne **asal business (core work)** par focus kar sakti hai.
6. **Go Global in Minutes**
  AWS ke paas duniya bhar mein data centers (regions) hain chand clicks mein aap apni application **kisi bhi mulk mein** deploy kar sakte hain.

---



## Summary


| Concept   | Asal Baat                                                 |
| --------- | --------------------------------------------------------- |
| **IaaS**  | Sirf infrastructure milta hai, baki sab khud manage karo  |
| **PaaS**  | Sirf code do, baki AWS manage kare                        |
| **SaaS**  | Sab kuch ready-made, bas use karo                         |
| **CapEx** | Bara, one-time kharcha (khareedne se pehle pay)           |
| **OpEx**  | Chhota, ongoing kharcha (jitna use utna pay)              |
| **TCO**   | Kisi cheez ka poora, asal kharcha (included hidden costs) |


