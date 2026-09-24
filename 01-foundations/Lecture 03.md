# Cloud Deployment Models, Design Principles & Well-Architected Framework

---

## Cloud Deployment Models

### Example:

- **Amazon, Google Cloud** companies banati hain.
- Company's example: jab **traffic zyada hoti thi**, to **2-3 servers use hote the**.
- Jab traffic kam ho jati thi, to wo **extra servers "useless" ho jate the** phir bhi unka kharcha uthana parta tha.
- **AWS ka solution:** **"Pay as you go"** server **cloud se le lo**, jitna **use karo utna hi pay karo**. Zaroorat khatam ho to server chhor do, extra paisa nahi dena.

### Safety/Security

- Data ko **cloud mein save karna** matlab data **kisi aur ke server par** rakhna hota hai.
- *Misal:* **Bank** apna data cloud/web par store karta hai **data center ke server** use hote hain.
- Is mein risk: **Data leakage** (data leak hone ka risk) kyunke data third-party server par hota hai.



### Cloud Deployment Models (3 Types)

1. **Cloud (Cloud-only)**
  - **"No use of own server"** company **apna koi bhi physical server nahi rakhti**.
  - Sab kuch (data, app, website) **poori tarah cloud provider (jaise AWS) par host** hota hai.
2. **On-Premises**
  - Company **apna website/app khud apne server par host karti hai** apna data center/infrastructure khud manage karti hai.
  - Cloud use nahi hota, sab kuch **company ke apne setup mein** hota hai.
3. **Hybrid**
  - **Sensitive data apne server par** rakha jata hai (security ke liye), aur **baki (non-sensitive) cheezein cloud par** rakhi jati hain.
  - Ye **on-premises aur cloud ka mix** hota hai jahan sensitive/confidential data local rehta hai, aur baki scalable cheezein cloud par.

> **Simple Yaad:** Cloud = sab kuch cloud par | On-Premises = sab kuch khud ke server par | Hybrid = dono ka mix (sensitive data khud ke paas, baki cloud par)

---


## Design Principles



### 1. Scalability

Scalability ka matlab hai **system ki capacity ko zaroorat ke according increase krna.**

- **Vertical Scaling ("Scale Up"):**
  - **Ek hi server** par uski **machine ke andar cheezein upgrade** ki jati hain jaise **RAM, CPU** barhana.
  - Simple: **usi server ko "powerful" bana dena**.
- **Horizontal Scaling ("Scale Out"):**
  - **Server/machines ki quantity incraese krna {Left, Right server add krna}** jaise **RAM, SSD/HDD, aur naye servers add karna**.
  - *Misal:* Zaroorat parne par **extra servers add kar dena**.
- **Preferred Method: Load Balancer**
  - Ek **akela server** sab kuch handle nahi karta is liye **Load Balancer** use hota hai.
  - Load Balancer **multiple servers ke middle traffic ko divide/manage karta hai**, taake koi ek server overload na ho.



### 2. Elasticity

Elasticity ka matlab hai **demand ke according automatically resources kam ya zyada hona**.

- *Misal:* Website ka **traffic kabhi barh jata hai, kabhi kam ho jata hai** **AWS is demand ke hisaab se khud scale karta hai**.
- Kisi **event/sale** ke waqt agar traffic achanak barh jaye, to AWS **naye servers automatically add kar deta hai** Example: **5 se lekar 20 servers tak** ja sakta hai.
- Jab traffic **zyada ho jata hai to divide ho jata hai** (multiple servers mein divide kr diya jata hai).
- **Baad mein jab traffic normal ho jaye**, to **extra/slow servers automatically remove** ho jate hain.
- **Billing bhi "pay as you go" par based hoti hai** AWS khud manage karta hai ke kitne resources chahiye, aur **sirf utna hi charge karta hai**.

> **Difference:** Scalability = capacity barhane ki **ability** (manual ya planned bhi ho sakta hai). Elasticity = **automatically** demand ke according resources ka kam/zyada hona (real-time).

---



## High Availability (HA)

- **High Availability** means: **servers/system hamesha available ho** down na ho.
- **Machine ka "up and running"** rehna zaroori hota hai, taake system **hamesha kaam karta rahe**.
- Iske liye **backup company (jaise AWS) ke paas hota hai** agar koi problem aaye to backup se kaam chal jata hai.
- **1 Point of Failure (Single Point of Failure) na ho** is design principle ka purpose ye hota hai ke agar **koi ek part/server fail ho jaye**, to poora system down nahi hota.
- Agar **ek part fail ho jata hai**, to system **automatically dusre (new/healthy) server par shift ho jata hai** user ko koi farak nahi parta.

> **Simple:** Agar ek server crash ho jaye, to traffic khud-ba-khud doosre working server par chala jata hai website down nahi hoti.

---



## AWS Well-Architected Framework (6 Pillars)

Ye **AWS ka official rulebook** hai achay cloud systems banane ke liye. Ye koi database concept nahi **ye AWS ki apni cheez hai**,  Isme **6 pillars** hain inhein **kisi bhi system ke liye 6 quality checks** samjho.


| #   | Pillar                     | Simply                                                                                             |
| --- | -------------------------- | -------------------------------------------------------------------------------------------------- |
| 1   | **Operational Excellence** | Systems ko achi tarah chalana aur monitor karna; hamesha behtar banate rehna; kaam automate karna. |
| 2   | **Security**               | Data aur systems ko secure karna; control karna ke kaun kya access kar sakta hai.                  |
| 3   | **Reliability**            | System failure se recover ho jaye aur zaroorat ke waqt kaam kare.                                  |
| 4   | **Performance Efficiency** | Computing resources ko sahi tarah use karna; fast rehna; waste na karna.                           |
| 5   | **Cost Optimization**      | Extra kharcha na karna; sirf utna hi pay karna jitni zaroorat hai.                                 |
| 6   | **Sustainability**         | Environment par asar kam karna; energy ko efficiently use karna.                                   |




### Memory Hook

> **"Operate Securely Reliable, Performant, Cheap, Sustainable."** → **O, S, R, P, C, S**

---



## Summary


| Concept                        | Simple                                                                                                                     |
| ------------------------------ | -------------------------------------------------------------------------------------------------------------------------- |
| **Cloud Deployment (Cloud)**   | Sab kuch cloud par, apna server nahi                                                                                       |
| **On-Premises**                | Sab kuch apne server par                                                                                                   |
| **Hybrid**                     | Sensitive data apne paas, baki cloud par                                                                                   |
| **Vertical Scaling**           | Ek server ko powerful banana (RAM/CPU increase)                                                                            |
| **Horizontal Scaling**         | Zyada servers add karna                                                                                                    |
| **Load Balancer**              | Traffic ko multiple servers mein divide karta hai                                                                          |
| **Elasticity**                 | Demand ke according automatic scale (up/down)                                                                              |
| **High Availability**          | System hamesha runing rahe, single point of failure na ho                                                                  |
| **Well-Architected Framework** | AWS ke 6 pillars: Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization, Sustainability |


