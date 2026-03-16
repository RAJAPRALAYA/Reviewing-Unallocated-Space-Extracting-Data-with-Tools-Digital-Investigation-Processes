# Reviewing-Unallocated-Space-Extracting-Data-with-Tools-Digital-Investigation-Processes
## AIM:
To review unallocated space in a disk image, extract data using forensic tools, and understand the digital investigation process.
## REQUIREMENTS
- Autopsy or FTK Imager
- Sleuth Kit (TSK)
- Hex Editor (e.g., HxD)
- Operating System: Windows 10/11 or Linux (Kali preferred)
## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Load into Autopsy or Sleuth Kit]
    B --> C[Identify Unallocated Space]
    C --> D[Scan for Data Signatures]
    D --> E[Carve and Recover Files]
    E --> F[Analyze Recovered Data]
    F --> G[Document Findings in Report]
```
## DESIGN STEPS:
### Step 1 (Acquire Evidence Image):
- Obtain the disk image in ```.dd``` or ```.E01``` format from a trusted forensic acquisition process.
- Verify hash values (MD5/SHA256) to maintain integrity.

### Step 2(Load Image into Forensic Tool):
- Open Autopsy or FTK Imager.
- Create a new case and add the evidence image.

### Step 3(Locate Unallocated Space):
- Navigate to the partition structure view.
- Identify sectors not assigned to any partition (unallocated).
### Step 4(Analyze & Carve Data):
- Use built-in data carving tools to search for file signatures (JPEG, DOCX, PDF, etc.).
- Preview carved files for relevance.
  
## PROGRAM:
| Step | Action                     | Tool Used                   | Output                       |
| ---- | -------------------------- | --------------------------- | ---------------------------- |
| 1    | Load disk image            | Autopsy / FTK Imager        | Partition & unallocated view |
| 2    | Identify unallocated space | Autopsy File System View    | Sector ranges                |
| 3    | Data carving               | Autopsy Data Carving Module | Recovered files              |
| 4    | Export evidence            | Autopsy Export Option       | File copies for analysis     |


## OUTPUT:
Unallocated Space Analysis and Extracted Data Report
<img width="1030" height="785" alt="Screenshot 2025-10-10 175428" src="https://github.com/user-attachments/assets/2ac38c8b-80db-4565-b3c1-d2d6be659753" />

<img width="964" height="656" alt="Screenshot 2025-10-10 175440" src="https://github.com/user-attachments/assets/6c95d1e7-3f21-4e15-953f-a9e5d85ef619" />

<img width="1019" height="343" alt="Screenshot 2025-10-10 175449" src="https://github.com/user-attachments/assets/a018a50a-e3c0-412d-bb6e-053325bc2a59" />
<img width="1002" height="505" alt="Screenshot 2025-10-10 175502" src="https://github.com/user-attachments/assets/31980ff8-aa69-46b9-a0d0-9de26e8a0a44" />
<img width="1006" height="515" alt="Screenshot 2025-10-10 175511" src="https://github.com/user-attachments/assets/688a33f7-c6f2-495a-b0a5-80b9b408861f" />

<img width="679" height="404" alt="Screenshot 2025-10-10 180009" src="https://github.com/user-attachments/assets/3038eb08-8197-42a6-a166-95f391d44e77" />

## RESULT:
The unallocated space was successfully analyzed, data was extracted, and the digital investigation process was followed effectively.

