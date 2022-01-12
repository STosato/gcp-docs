# Storage & Database Services
## Storage Services
- Unified object storage for a variety of applications  
• Applications can store and retrieve objects through single API  
• GCS can scale to exabytes of data   
• Data can be stored within a single region, dual-region, or multi-region

![[storage-services.png]]
### Persistent disks
- Independent (out of the context) from compute engine VMs
- Only one writer, multiple readers
- Can be replicated in **regional** or **local**
### Cloud Filestore
- **Managed**
- For **legacy** apps
- Shared & NAS-like filesystem
- for GCE e GKE
- Useful for [[on-premises]] applications
- Zonal storage for **replications**
- encrypted

```mermaid
graph TD

 A[Bucket] -->B(Folder)

 A-->C[Folder]

 C --> D[File]

 C --> E[File]
```
![[Pasted image 20211230165549.png]]

![[database_services]]