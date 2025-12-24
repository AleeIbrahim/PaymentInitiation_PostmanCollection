# Payment Initiation Postman Collection

This repository contains the Postman collection for the **Payment Initiation API**, including mock server setup, and test execution commands.

---

## **1. Collection Import Instructions**

To import the collection into Postman:

1. Download the `Payment-initiation-API.postman_collection.json` file from this repository.  
2. Open Postman → click **File → Import** or **Import** button in the top-left corner.  
3. Select **Upload Files** and choose the JSON collection file.  
4. The collection will appear in your Postman workspace, ready to use.  

> **Optional:** Import the environment file (`New-Mock-Server.postman_environment.json`) if the requests require environment variables.  

---

## **2. Mock Server Setup Steps**

If you want to run the collection against a mock server:

1. Open Postman → go to **Collections** → select the collection → click **Mock Server**.  
2. Click **Create a mock server**.  
3. Configure the mock server:
   - **Name:** Payment Initiation Mock  
   - **Environment:** Optional  
4. Copy the generated mock server URL.  
5. Update your collection or environment to use the mock server URL for requests.  

---

## **3. Test Execution Commands**

### **Option 1: Run in Postman**
- Click **Collection → Run** → select environment → click **Run Collection**.  

### **Option 2: Run via Newman (CLI)**
1. Install Newman globally (if not already installed):
   ```bash
   npm install -g newman

2. Run the collection

   ```bash
   newman run Payment-initiation-API.postman_collection.json -e New-Mock-Server.postman_environment.json -d payment-test-data.json -r cli,html,json --reporter-html-export TestReport.html

---

## **4. Validation Rules Summary**
- HTTP Status Codes: Ensure expected response codes (200, 201, 400, etc.).
- Field Validations: Key fields like iban, amount, and status are checked for correctness and type.


