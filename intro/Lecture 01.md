# Amazon Web Services (AWS) – Cloud Security Engineering

---

## 1. Before Cloud 

- Tqreeban **80% data store karne ka kaam** company **khud** karti thi koi outsource solution nahi tha.
- Har company jise data save karna hota tha, usay apna **khud ka infrastructure** banana aur manage karna parta tha.

## 2. Purana (On-Premises) Model

- Companies khud hi **"server buy karne wali party"** hoti thin unhein physical servers khareedne parte the.
- Data seedha inhi company-owned servers mein store hota tha.
- Taqreeban har organization/unit ko apna alag **server room** rakhna parta tha.
- Ye sab chalane ke liye company ko chahiye hota tha:
  - **Hardware**
  - **Servers**
  - Inhein rakhne ke liye **physical space**



### Costs of Owning Your Own Servers

Apne servers khud khareedna sirf ek computer lene jaisa nahi tha is mein bohat se recurring aur **"expensive"** kharche shamil the:


| Cost Type                | Details                                                                                                                           |
| ------------------------ | --------------------------------------------------------------------------------------------------------------------------------- |
| **Server Configuration** | Zyada data ki zaroorat ho to zyada computers aur kaafi **expensive** server configuration chahiye hoti thi.                       |
| **Purchase Cost**        | Server hardware khareedna hi apne aap mein bara investment tha.                                                                   |
| **Bijli/Server's Bill**  | Server chalate rehne ke liye recurring bijli aur maintenance ka kharcha.                                                          |
| **Cooling**              | Servers garam hote hain, is liye unhein thanda rakhne ke liye **AC aur fan** chahiye hote hain, warna server kharab ho sakta hai. |
| **Staff/Room**           | Server room aur unko maintain karne wale log alag se chahiye hote the.                                                            |


**Shortly:** apne servers khud chalana matlab bara upfront investment + continuous maintenance + cooling + staff ka kharcha chahe capacity poori use ho ya na ho.

## 3. Amazon's Solution

- Amazon ne apne bohat bare **data centers** banaye.
- Ab har company ko khud server khareedne aur maintain karne ki zaroorat nahi Amazon companies ko **server capacity rent par deta hai**.
- **Pay-as-you-go model:** Server jab tak use ho raha hai, tab tak paise lagtay rehtay hain.
  - For Example: agar server 2 din use na ho, phir bhi customer ko un 2 dino ka payment karna parta hai (billing usage/uptime ke hisaab se hoti hai, sirf active kaam ke hisaab se nahi).
- Companies in remote servers ko internet ke through securely access karti hain, aksar **VPN** ke through apne physical hardware rakhne ki bajaye.



## 4. The Real Point

Yehi **cloud computing** aur **AWS (Amazon Web Services)** jaisi services ka fundamental (core) idea hai:

> Har company ke apne server khareedne, rakhne, thanda karne aur maintain karne ki bajaye, Amazon khud bare data centers rakhta aur maintain karta hai, aur companies sirf apni zaroorat ke hisaab se **computing/storage resources rent par** leti hain, secure tareeqay se access karti hain (jese VPN se), aur sirf utna hi paisa dete hain jitna use karte hain.

Is changing (shift) se companies ko in cheezon ki tension nahi rehti:

- Hardware khareedna
- Server rooms banwana
- Cooling systems (AC/fan)
- Physical maintenance aur bijli ke bills

...aur is ki jagah ek flexible, scalable, pay-per-use cloud model aa jata hai jo **AWS Cloud Security Engineering** ki foundation hai.

---

