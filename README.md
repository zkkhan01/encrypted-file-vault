# Encrypted File Vault - Enterprise-Grade Secure Document Storage

This project is a security-focused prototype demonstrating how to build an encrypted document vault similar to Dropbox/Google Drive but with **client-side AES encryption**, **PBKDF2 per-user keys**, **RBAC**, **audit logging**, and **S3 presigned URLs**.

## 🚀 Architecture Overview
See `diagram.svg` in the repository.  
- Client encrypts files using AES-256  
- Keys derived per user via PBKDF2  
- Server issues presigned S3 URLs  
- RBAC governs file access  
- Audit logs track actions  

## 🧪 Example Workflow
1. User uploads file → client encrypts  
2. Server derives per-user key signature  
3. Upload via S3 presigned URL  
4. Access logged + dashboard view  

## 🔧 Setup & Run
```
pip install -r requirements.txt
uvicorn backend.main:app --reload
```

## ✅ Status
Prototype / POC
