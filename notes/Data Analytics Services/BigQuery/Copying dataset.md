# Copying dataset
Once created, a dataset **can't change location**. The only way to do that is **making a copy**.

First,

## 1. Enable BigQuery Data Transfer API
Sidebar > APIs & Services > Enable APIs & Services > search "BigQuery Data Transfer API" > Enable

## 2. Create a new dataset
"Create Dataset" button

## 3. Copying the dataset
Go to the **source dataset** and click "copy dataset"
!["alt"](../../Images/copyDataset1.png)

Then select **destination**

!["alt"](../../Images/CopyDataset2.png)

# Scheduling 
Left menu > Transfers > Create Transfer

Source: **dataset copy**

set Transfer Config Name

set **timing**

In the **destination**: the **dataset ID**

### Limitations
- only **one active copy** at time
- can't copy:
	- views
	- external tables
	- streaming buffer

