# Azure-website-hosting
Azure-website-hosting

# Azure Static Website Hosting Project

## Overview
This project demonstrates how to host a static website using Azure Blob Storage static website hosting.

The solution eliminates the need for a traditional web server by serving content directly from Azure storage.

---

## Architecture

- Azure Storage Account (General Purpose v2)
- Blob Storage (Hot tier)
- Static Website Hosting
- $web container

---

## Deployment Steps

1. Created a Storage Account using Microsoft Azure Portal
2. Selected:
   - Performance: Standard
   - Redundancy: Locally Redundant Storage (LRS)
3. Enabled Static Website Hosting
4. Configured:
   - Index document: index.html
   - Error page: 404.html
5. Uploaded files to $web container:
   - index.html
   - 404.html
   - Images (coffee.jpg, beach.jpg)
6. Accessed the live endpoint

---

## Live Website

🔗 https://asiwajustorageaccount.z13.web.core.windows.net/

---

## Screenshots

(Add your screenshots here)

---

## Storage Configuration

### Performance Tier: Standard

The Standard tier uses magnetic disk-backed storage and is optimized for cost efficiency.

**Impact:**
- Lower cost compared to Premium
- Suitable for static websites with moderate traffic
- Slightly higher latency than Premium, but negligible for this use case

---

### Redundancy: Locally Redundant Storage (LRS)

LRS replicates data three times within a single Azure data center.

**Impact:**
- Lowest storage cost option
- Protects against hardware failure within a data center
- Does NOT protect against regional outages

---

## Cost Optimization

- Used Standard performance tier to minimize cost
- Selected LRS redundancy for cheapest replication
- No compute resources (VMs) required
- Pay only for storage and bandwidth

---

## Security Considerations

- HTTPS enforced via Azure endpoint
- No server exposure (reduced attack surface)
- Public read access limited to static content only

---

## Scalability

- Automatically scales based on demand
- Can integrate with Azure CDN for global performance improvement

---

## Limitations

- No server-side processing (HTML/CSS/JS only)
- No backend logic

---

## Conclusion

Azure Blob Storage static website hosting provides a highly cost-effective, scalable, and secure solution for hosting static web applications.

This project demonstrates a fully functional deployment using best practices for cost optimization and simplicity.
