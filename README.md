# Cloud Infrastructure Cost Comparison: AWS vs. Azure

## 1. Application Specifications (Task 1)
For this analysis, we modelled a small-scale web application with the following technical requirements:
* **Instances:** 4 Virtual Machines
* **Compute:** 4 vCPUs and 16 GiB RAM per instance
* **Storage:** 100 GB SSD (gp3 for AWS / Premium SSD for Azure)
* **Region:** Africa (Cape Town / South Africa North)

## 2. AWS Cost Breakdown (Task 2)
Using the AWS Pricing Calculator, we selected the **t4g.xlarge** instance type.
* **OS:** Linux
* **Pricing Strategy:** On-Demand
* **Monthly Total:** **$506.33 USD**
* *Note: This estimate includes the 4 instances and baseline storage as configured in the project screenshots.*

## 3. Azure Cost Breakdown (Task 3)
Using the Azure Pricing Calculator, we selected the **D4s_v5** instance type.
* **OS:** Windows
* **Feature:** Azure Hybrid Benefit (Applied)
* **Monthly Total:** **$284.00 USD**
* *Comparison:* Azure provides a significant cost reduction by waiving the Windows licensing fee through the Hybrid Benefit.

## 4. Networking & Inter-Zone Costs (Task 4)
We analysed the potential data transfer fees for a multi-zone deployment:
* **AWS & Azure:** Both providers charge approximately **$0.01 per GB** for data transfer between availability zones. 
* **Impact:** For 500GB of inter-zone sync, an additional $10.00/month should be budgeted for either platform.

## 5. Discount Mechanisms (Task 5)
* **AWS Savings Plans:** Offers up to 72% savings in exchange for a 1 or 3-year hourly spend commitment.
* **Azure Reserved Instances:** Offers similar savings for committing to specific VM sizes in a specific region.

## 6. Cost Optimisation Strategies (Task 6)
1. **Spot Instances:** Utilising Spot VMs for non-critical tasks can save up to 90% over the costs shown in this report.
2. **Storage Optimisation:** Using **gp3** on AWS and manually setting IOPS can prevent paying for unused performance overhead.
