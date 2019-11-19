
# For Supply Chain part


### Step 1: Distributor (Mobile Network Operator) issue `Schema`s to indy ledger
`IoT Device Schema`, Schemas are on the ledger (public for everyone)

### Step 2: Producer (Manufacturers) create `Credential Definitions`
`Production IoT device Credential Definitions ` (based on IoT Device Schema), issue to indy Ledger.

### Step 3: Producer (Manufacturers) create `Schema` to Indy ledger
`Production QA Schema`

### Step 4: QA team create `Credential Definitions` 
`QA qualification Credential Definitions` (based on `Production QA Schema`)

### Step 5: a new IoT device, Alice, obtains `Credential` from Producer (Manufacturers)
1.	On boarding device with Manufacturers

2.	Manufacturers send `Credential Offer` to device

3.	Device retrieves `Tele IoT device Credential Definitions` from ledger, and send `Credential Request` to Manufacturers

4.	Manufacturers creates `Credential` to device, assigned the series number

5.	Device store the credential in device’s wallet.

(This corresponds to GSMA’s Stage #1 #2)

### Step 6: a new IoT device (default ownership is Manufacturers), obtains` Credential` from Producer (Manufacturers)

1.	On boarding device with QA team

2.	QA team send `Credential Offer` to device

3.	Device retrieves ` QA qualification Credential Definitions` from ledger, and send `Credential Request` to QA team

4.	QA tram creates `Credential` to device (If device pass the QA test)

5.	Device store the credential in device’s wallet.

(This corresponds to the GSMA’s #3 #4)

### Step 7: Distributor requests proof of QA from QA team
1.	On boarding distributor and device

2.	Distributor create a `Proof Request`

3.	Device receives this `Proof Request`, create a `Proof` based on the credential obtaining from Tele Company 

4.	Distributor receive the `Proof`, and verify if fulfills the requirement.

5.	Distributor Accept the `Proof` and issue an MSISDN (with DID)

6.  The ownership change to distuibutor

(This corresponds to the GSMA’s #5 #7)

### Step 8: The Ownership of IoT device change to the end user

1.	User requests activation from distributor, to simplify the problem, we skip the KYC process, distributor create a `Proof Request` for KYC and receive the `Proof` from user

2.	Distributor mark MSISDN DID with the ownership of user

3.	Producer mark user’s DID as owner of the device

 (This corresponds to the GSMA’s #9 #10)

# For the device-to-device access control:
1.	The owner of Device Alice mark `allow` for Device Bob’s DID in Alice’s DID Document

2.	When Bob connect to Alice, determine if it is allowed


More graph to illustrate will be assigned here.
