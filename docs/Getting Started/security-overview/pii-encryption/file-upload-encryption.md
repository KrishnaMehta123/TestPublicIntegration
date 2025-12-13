---
title: File Upload Encryption
excerpt: >-
  Learn about secure handling of uploaded files through robust encryption
  protocols applied during transfer and storage.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

File Upload Encryption enables you to securely and automatically bring data from an external server into your system. You can use it to ingest structured files such as user data, events, or configuration files in CSV or JSON format from trusted external sources into your platform.

With File Upload Encryption, you can set up scheduled imports or trigger them as required, ensuring timely and secure data input while aligning with your security and compliance standards. The import setup supports authentication through SSH keys

File upload Encryption supports Pretty Good Privacy (PGP) encryption, adding an extra layer of protection by ensuring that sensitive data remains encrypted throughout the transfer, safeguarding its confidentiality and integrity until CleverTap successfully processes it.

File Upload Encryption is beneficial in the following scenarios:

* **Preventing data leaks during transit**: It prevents interception of data files during upload.
* **Addressing security concerns**: Offers stronger protection through encryption and complies with data privacy and security regulations.
* **Preventing misuse**: Encrypted files remain unreadable to unauthorized users in the unlikely event of a breach.

> 📘 Private Beta
>
> File Upload Encryption is available in Private Beta. To enable this feature, contact your Customer Success Manager or raise a support ticket.

# Prerequisites

A configured and connected SFTP client to CleverTap's SFTP server is the prerequisite for achieving File Upload Encryption.

<Image alt="SFTP Export" align="center" border={true} src="https://files.readme.io/cc3c3ea314b2e0e72d7caaab4ad21ec03f5ecdd0b6f0364bb77d629e3330a671-image.png">
  File Upload Encryption
</Image>

# Secure File Upload with PGP Encryption

Prepare the data file in plain text format to upload into the CleverTap database. 

To encrypt and securely upload your data using PGP over SFTP, perform the steps below:

1. [Generate PGP Key Pair ](doc:file-upload-encryption#generate-a-pgp-key-pair)
2. [Receive the Key ID](doc:file-upload-encryption#receive-the-key-id)
3. [Create Manifest File](doc:file-upload-encryption#create-the-manifest-file)
4. [Upload Encrypted File and Manifest via SFTP](doc:file-upload-encryption#upload-encrypted-file-and-manifest-via-sftp)

## Generate a PGP Key Pair

CleverTap supports PGP encryption for secure file uploads via SFTP and other supported import methods. Using PGP encryption adds a layer of security, ensuring that sensitive data remains protected throughout the transfer and ingestion process. 

**Prerequisites**

The following are the prerequisites for File Upload Encryption using PGP key generation: 

* **Public key** -   Used by the user to encrypt `.csv` files.
* **Private Key** - Used by CleverTap to decrypt uploaded files.
* **Passphrase**- A secure password set by you that allows CleverTap to access the private key.

> 📘 Sharing Private Keys
>
> The private key must be shared only with authorized individuals, as it provides access to sensitive and confidential data.

You can generate a PGP key pair in one of two ways:

* [Self-generated](doc:file-upload-encryption#self-generated-keys).
* [CleverTap generated](doc:file-upload-encryption#clevertap-generated-keys).

### Self-Generated Keys

The following steps describe how to use PGP encryption through GnuPG, a free implementation of the PGP standard.

To generate your own PGP key pair using the gpg command-line tool, follow the steps below:

```asp Customer-generated Keys
--# Step 1: Generate the key
gpg --full-generate-key

# Step 2: Select key type
# (1) RSA and RSA
# (2) DSA and Elgamal
# (3) DSA (sign only)
# (4) RSA (sign only)
# (9) ECC (sign and encrypt) *default*
# (10) ECC (sign only)
# (14) Existing key from card
# Choose option 1 (RSA and RSA)

# Step 3: Key size
# Enter: 3072 (recommended)

# Step 4: Key expiration
# Enter: 0 (key never expires)
# Confirm: y

# Step 5: Enter user ID details
# Name: Name1
# Email: email1@company1.com
# Comment: (optional)
# Confirm selection: O
```

#### Create Passphrase

After you create the public key and private key, the system prompts you to set a passphrase. Note this passphrase, as it is required later during decryption.

#### Confirm Key Generation

After successfully creating the key, GPG generates public and private keys and a revocation certificate

```asp Key Creation Confirmation
# gpg: revocation certificate stored as '/root/.gnupg/openpgp-revocs.d/1A7849F996BFD78569533B2CF55DEEE68995217D.rev'
# public and secret key created and signed.
# pub   rsa3072 2024-11-21 [SC]      1A7849F996BFD78569533B2CF55DEEE68995217D
# uid                      Name1 <email1@company1.com>
# sub   rsa3072 2024-11-21 [E]
```

#### Export the Private Key Using the Public Key

After successfully generating your PGP key pair, you must share the private key with CleverTap, this enables CleverTap to decrypt your encrypted files during import.

Use the following command:

```asp Export the Private Key
gpg --export-secret-key -a "your-key-id" > private.key
```

* `"your-key-id"` – Replace this with your public Key generated earlier. 

This is the **Public Key** of the public/private key pair you generated using GPG. You can find it in the confirmation message after generating your keys.

For example,

```asp
 pub   rsa3072 2024-11-21 [SC]  1A7849F996BFD78569533B2CF55DEEE68995217D
```

In this case, `1A7849F996BFD78569533B2CF55DEEE68995217D` is your Public key.

* `private.key` – Name of the `.key` file that contains the exported private key.\
  This is the name you provide to the `.key` file when exporting your private key. It contains the key in a readable text format. CleverTap uses this file (along with the passphrase) to decrypt any data you upload in encrypted form.

> 🚧 Security Tip
>
> Store the `private.key` file securely and share it only with authorized personnel or platforms. Anyone with access to this file and the passphrase can decrypt your data.

#### Encrypt CSV File using PGP

Once you have generated your PGP key pair, the next step is to encrypt the data file (`.csv` format) using your public key. This step ensures the file is secure during transit and can only be decrypted by CleverTap using the associated private key.

To encrypt your CSV file, execute the command below:

```asp Encrypt CSV File
gpg --encrypt --armor -r email@company.com --vv /Users/Desktop/filename.csv
```

> 📘 Best Practice
>
> Ensure the `.csv` file is final and formatted properly before encryption. Once encrypted, you cannot modify its contents.

The encrypted file has a `.asc` file, for example, `users_data.csv.asc`. It is ready for upload along with the corresponding manifest file via SFTP.

### CleverTap-Generated Keys

CleverTap generates a PGP key pair for you and securely shares the public key, private key, and passphrase. It also provides a Key ID, a unique reference to identify the key set.

> 📘 Request for Encryption Keys(Public & Private keys) and Key ID
>
> Reach out to your CSM or raise a support ticket to receive the required credentials.

#### Key ID

CleverTap generates a KeyID, that you must include in your manifest file, after you upload your Encryption keys. This ID is required in your manifest file to allow CleverTap to identify and use the correct encryption key.

**Sample IDs:**

* Private Key ID: `1A7849F996BFD78569533B2CF55DEEE68995327F`
* Key ID: `ec491319-9823-48cd-b6a1-6bb0bc666d75`

## Receive the Key ID

Share your encryption keys (public & private) and passphrase with CleverTap. 

> 📘 Sharing keys & passphrase with CleverTap
>
> Reach out to your CSM or raise a support ticket with the encryption keys & passphrase to receive the Key ID.

## Create the Manifest File

The manifest file contains metadata about your encrypted file, which conveys to CleverTap how to interpret the uploaded file. Ensure the `fileName` field uses the `.asc` extension. Create the manifest file in JSON/YAML format. The manifest file is critical for proper ingestion and mapping and holds the following information:

* Reference to the encrypted .asc file path
* The Key ID (provided by CleverTap) to indicate which key to use for decryption
* Field mappings (for example, email → identity, timestamp → TS)
* Data type (for example, profile or event)

The following is the sample manifest file:

```json
{  
  "fileName": "parastest31.csv.asc",  
  "type": "event",  
  "columns": {  
    "event_name": { "ctName": "evtName", "dataType": "String" },  
    "time_stamp": {"ctName": "ts", "dataType": "Integer"},  
    "identity": {"ctName": "identity", "dataType": "String"},  
    "item_name": { "ctName": "Name", "dataType": "String" },  
    "item_price": {"dataType": "Integer"},  
    "item_delivery_date": { "ctName": "DeliveryDate", "dataType": "String" }  
  },  
  "clientEmail": "[User@clevertap.com](mailto:User@clevertap.com)",  
  "keyId": "ec491319-9823-48cd-b6a1-6bb0bc666d75"// Mention the KeyID here  
}
```

## Upload Encrypted File and Manifest via SFTP

Encrypt the .csv file using the public key before uploading vSFTP. The result is a .*asc* file (for example, `users_data.csv.asc`) in PGP-encrypted format. This encrypted file is not readable without the private key.

Connect to CleverTap's SFTP server using your private key:

`sftp -i ~/.ssh/id_rsa username@serverURL`

`put filename.csv.asc`

`put file.manifest`

> 🚧 File Size Limit
>
> Ensure the encrypted file is less than 1 GB. Split larger files into smaller parts.

# Decryption and Ingestion by CleverTap

CleverTap processes the uploaded data securely and integrates it into the platform.\
CleverTap uses the provided Key ID to look up the following:

* Private key
* Passphrase

The *.asc* file is decrypted securely within CleverTap's environment.

Once decrypted, the data is parsed using manifest mappings and ingested into user profiles or event streams.

# Email Notifications

You receive email notifications at the following stages of the File Upload Encryption process:

* **File Pickup:** The system successfully picks up your file for processing.
* **Successful Import:** The system uploads and processes your file successfully.
* **Import Failure:** The system sends an email with error details, including the specific column affected and a clear description.

# Additional Resources

* For more information on File Upload Encryption, refer to the [Import via SFTP](https://developer.clevertap.com/docs/imports-via-sftp).

# FAQs

### What types of data can I import via SFTP?

You can import **user data** and **event data** in CSV or JSON formats.

### What are the file size limits for File Upload Encryption?

The encrypted file must be below 1 GB. Split larger files before uploading.

### Who generates the `key_id`?

CleverTap generates and shares the `key_id` after storing your keys.

### What is a manifest file, and why is it needed?

A manifest file is a JSON file that describes your uploaded data file. It includes the file name, data type, column mappings, and Key ID.

### Can I schedule recurring encrypted file uploads?

Yes, you can schedule recurring encrypted file uploads. CleverTap ingests the file each time it is uploaded.

### How long does data import take?

Data import typically completes within a few minutes; however, the exact time may vary depending on the file size and system load. Once processing is complete, you will receive an email notification.

### Can I import multiple files at once?

Yes, but each file must be accompanied by its manifest file.

### How many encryption keys can I store or use?

You can store and manage up to 20 keys per account.
