# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:
Recovered Deleted File List and Details
<img width="1533" height="819" alt="WhatsApp Image 2026-11-02 at 12 51 32 PM" src="https://github.com/user-attachments/assets/b378fdca-9242-4fac-97ec-50f2655c958e" />
<img width="1535" height="814" alt="WhatsApp Image 2026-11-02 at 12 51 58 PM" src="https://github.com/user-attachments/assets/b4b4c581-f103-4a94-863b-70886a14f9b0" />
<img width="1535" height="815" alt="WhatsApp Image 2026-11-02 at 1 03 12 PM" src="https://github.com/user-attachments/assets/42ab3e3d-b41c-4e00-9f31-a40978fb37a2" />
<img width="1535" height="823" alt="WhatsApp Image 2026-11-02 at 1 04 02 PM" src="https://github.com/user-attachments/assets/dc5a755f-b110-4d1d-b7b7-523b2a88a8bf" />
<img width="1535" height="823" alt="WhatsApp Image 2026-11-02 at 1 04 02 PM" src="https://github.com/user-attachments/assets/91fd3330-74f9-4035-99b3-f5d696e76c82" />
<img width="1535" height="821" alt="WhatsApp Image 2026-11-02 at 1 05 40 PM" src="https://github.com/user-attachments/assets/c6522ca8-1368-40ff-b25e-932ec6fa68b0" />
<img width="1535" height="816" alt="WhatsApp Image 2026-11-02 at 1 13 04 PM" src="https://github.com/user-attachments/assets/c0f1d721-f765-441a-b833-e8e9e3d0ea44" />

## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
