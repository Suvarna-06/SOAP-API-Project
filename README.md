# 🚿 SOAP API Testing Project – *Number to Words Conversion*

---

## 👩‍💻 Author & Repository  
**Created by:** Sandhya Mohan Sankeshwar  
🔗 **GitHub Repository:** [Suvarna-06/soap-api-testing](https://github.com/Suvarna-06/soap-api-testing)

---

## 📝 Project Overview  
This project automates test cases for a **SOAP-based API** that converts **numerical values into their word format** using the `NumberToWords` method.  
Test scenarios include **positive, negative, and boundary validations** using **Postman** and **XML-based requests**.

---

## 🛠️ Tools & Technologies Used  
| Tool | Purpose |
|------|---------|
| 💻 Postman | Creating and executing SOAP requests |
| 📄 XML | SOAP body format |
| 🌐 SOAP Protocol | Web service communication |
| 📑 WSDL | Service definition |
| 💬 Newman (optional) | CLI execution |

---

## 📋 Test Plan Overview  
The test plan ensures full coverage of:

- ✅ **Positive Scenarios:** Conversion of various valid numeric inputs  
- ❌ **Negative Scenarios:** Invalid data types, missing headers, malformed XML  
- ⚠️ **Boundary Testing:** Extremely large numbers, zero, negative values  
- 🧪 **Error Handling:** XML validation errors, missing elements, unauthorized access  

---

## ✅ Highlighted Test Scenarios

| TC ID | Scenario | Input | Expected Output |
|-------|----------|-------|-----------------|
| TC01 | Valid Single Digit | `1` | "one" |
| TC02 | Two Digits | `34` | "thirty four" |
| TC05 | Large Number | `349989` | Word format |
| TC06 | Missing Headers | `223` | Error/500 |
| TC08 | String Input | `sandhya` | SOAP Fault |
| TC11 | Max Limit | `999999999999` | Delay/Error |
| TC13 | Beyond Range | `1000000000000000` | Fault |
| TC25 | Invalid XML | broken XML | Internal Server Error |

---

## ▶️ How to Run This Project

### 🔸 In Postman:
1. Import the collection: `Project #2 - SOAP.postman_collection.json`
2. Open **Collection Runner** → Select requests → Click **Run**

### 🔸 Using Newman CLI:
```bash
newman run Project_2_SOAP.postman_collection.json
