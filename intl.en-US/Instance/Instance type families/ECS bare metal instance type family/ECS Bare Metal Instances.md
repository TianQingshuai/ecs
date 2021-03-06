---
keyword: [Alibaba Cloud, ECS, server, elastic computing]
---

# ECS Bare Metal Instances

This topic describes the features of ECS Bare Metal Instance families and lists the instance types of each family.

-   Recommended instance families
    -   General purpose instance families:
        -   [ebmg6a, general purpose ECS Bare Metal Instance family](#section_vk4_ake_dah)
        -   [ebmg6e, general purpose ECS Bare Metal Instance family with enhanced performance](#section_69g_hx0_psw)
        -   [ebmg6, general purpose ECS Bare Metal Instance family](#section_qkb_ez6_9c5)
    -   Compute optimized instance families:
        -   [ebmc6a, compute optimized ECS Bare Metal Instance family](#section_m8p_b2e_yqq)
        -   [ebmc6e, compute optimized ECS Bare Metal Instance family with enhanced performance](#section_mdc_24m_q3e)
        -   [ebmc6, compute optimized ECS Bare Metal Instance family](#section_zec_q52_xn9)
    -   Memory optimized instance families:
        -   [ebmr6a, memory optimized ECS Bare Metal Instance family](#section_qwd_bje_kuu)
        -   [ebmr6e, memory optimized ECS Bare Metal Instance family with enhanced performance](#section_ltv_trm_b0o)
        -   [ebmr6, memory optimized ECS Bare Metal Instance family](#section_yv1_t65_log)
        -   [ebmre6p, non-volatile memory optimized ECS Bare Metal Instance family with enhanced performance](#section_xli_oah_7tq)
        -   [ebmre6-6t, memory optimized ECS Bare Metal Instance family with enhanced performance](#section_6kk_g42_kgh)
    -   Instance families with high clock speed:
        -   [ebmhfg6, general purpose ECS Bare Metal Instance family with high clock speed](#section_czp_w4q_mb8)
        -   [ebmhfc6, compute optimized ECS Bare Metal Instance family with high clock speed](#section_s0v_ihb_z5x)
        -   [ebmhfr6, memory optimized ECS Bare Metal Instance family with high clock speed](#section_sns_ot8_a1r)
    -   GPU-accelerated compute optimized instance families:
        -   [ebmgn6e, GPU-accelerated compute optimized ECS Bare Metal Instance family](#section_xyl_5bo_wez)
        -   [ebmgn6v, GPU-accelerated compute optimized ECS Bare Metal Instance family](#section_lke_80h_kzu)
        -   [ebmgn6i, GPU-accelerated compute optimized ECS Bare Metal Instance family](#section_slz_oyd_k1t)
-   Other available instance families
    -   [ebmg5s, general purpose ECS Bare Metal Instance family with enhanced network performance](#section_qiz_xda_sce)
    -   [ebmg5, general purpose ECS Bare Metal Instance family](#section_nii_o5k_4t2)
    -   [ebmc5s, compute optimized ECS Bare Metal Instance family with enhanced network performance](#section_pnq_v2c_u07)
    -   [ebmc4, compute optimized ECS Bare Metal Instance family](#section_8xi_1ce_45q)
    -   [ebmr5s, memory optimized ECS Bare Metal Instance family with enhanced network performance](#section_v7p_ot4_f4n)
    -   [ebmhfg5, ECS Bare Metal Instance family with high clock speed](#section_69a_h1f_n9m)

## Overview

ECS Bare Metal Instance is a compute service that combines the elasticity of virtual machines and the performance and features of physical machines. ECS Bare Metal Instance is designed based on the state-of-the-art virtualization 2.0 technology developed by Alibaba Cloud. The virtualization technology used by ECS Bare Metal Instance is optimized to support common ECS instances and nested virtualization. It maintains the elastic performance of ECS instances and the performance and features of physical machines.

ECS Bare Metal Instance combines the strengths of both physical machines and ECS instances to deliver powerful and robust computing capabilities. ECS Bare Metal Instance uses virtualization 2.0 to provide your business applications with direct access to the processor and memory resources of the underlying servers without virtualization overheads. ECS Bare Metal Instance retains the hardware feature sets \(such as Intel® VT-x\) and resource isolation capabilities of physical machines, which is ideal for applications that need to run in non-virtualization environments.

By virtue of the independently developed chips, hypervisor system software, and the redefined server hardware architecture, ECS Bare Metal Instance integrates features from both physical and virtual machines. ECS Bare Metal Instance can seamlessly connect with other Alibaba Cloud services for storage, networking, and database tasks. ECS Bare Metal Instance is fully compatible with ECS images. These properties allow you to build resources to suit your business requirements.

When you use ECS Bare Metal Instance, take note of the following items:

-   ECS Bare Metal Instance does not support instance type changes.
-   When the physical machine that hosts an ECS bare metal instance fails, the system fails the instance over to another physical machine. Data is retained within the data disks of the instance.

## Benefits

ECS Bare Metal Instance provides the following benefits based on technological innovations:

-   Exclusive computing resources

    As a cloud-based elastic computing service, ECS Bare Metal Instance delivers the same performance and resource isolation as standard physical machines and can ensure the exclusivity of computing resources without virtualization overheads or feature loss. ECS Bare Metal Instance supports 8, 32, 80, 96, or 104 vCPUs and high clock speeds. An ECS bare metal instance with eight vCPUs can provide a core frequency of 3.7 GHz to 4.1 GHz for better performance and faster response for gaming and finance businesses than peer services.

-   Chip-level security

    In addition to physical machine isolation, ECS Bare Metal Instance uses a chip-level trusted execution environment of Intel ® SGX to ensure that encrypted data can be computed only in a secure and trusted environment. This chip-level hardware security protection provides a safe box for your data in the cloud and allows you to control all data encryption and key protection processes. For more information, see [Install SGX](/intl.en-US/Instance/Instance type families/ECS bare metal instance type family/Install SGX.md).

-   Compatible with multiple private clouds

    ECS Bare Metal Instance can address the needs of high-performance computing and help you build new hybrid clouds. Thanks to the flexibility, elasticity, and other strengths inherited from the mix of physical and virtual machines, ECS Bare Metal Instance can implement re-virtualization. Offline private cloud business can be seamlessly migrated to Alibaba Cloud without performance overheads arising from nested virtualization, giving you a new method to move businesses onto the cloud.

-   Support for heterogeneous instruction set processors

    Virtualization 2.0 used by ECS Bare Metal Instance is developed independently by Alibaba Cloud, and supports instruction set processors such as ARM at no additional cost.


## Comparison of ECS bare metal instances, physical machines, and virtual machines

Compared with a physical machine with the same configurations, an ECS bare metal instance delivers greater performance. During Double 11, ECS bare metal instances delivered robust computing capabilities with millions of vCPUs to handle traffic spikes.

The following table describes a comparison among the features of ECS bare metal instances, physical machines, and virtual machines. In this table, Y means supported, N means not supported, and N/A means not applicable.

|Feature type|Feature|ECS bare metal instance|Physical machine|Virtual machine|
|:-----------|:------|:----------------------|:---------------|:--------------|
|Automated O&M|Delivery within minutes|Y|N|Y|
|Compute|Zero performance loss|Y|Y|N|
|Zero feature loss|Y|Y|N|
|Zero resource preemption|Y|Y|N|
|Storage|Compatible with ECS disks|Y|N|Y|
|Startup from system disks|Y|N|Y|
|Quick reset of system disks|Y|N|Y|
|Use of ECS images|Y|N|Y|
|Cold migration between physical and virtual machines|Y|N|Y|
|No need to install the operating system|Y|N|Y|
|No need of local Redundant Arrays of Independent Disks \(RAID\), and better protection of data in disks|Y|N|Y|
|Networking|Compatible with VPCs|Y|N|Y|
|Compatible with the classic network|Y|N|Y|
|No communication bottlenecks between physical and virtual machine clusters in VPCs|Y|N|Y|
|Management|Compatible with existing ECS management systems|Y|N|Y|
|Consistent user experiences on features such as VNC with that of virtual machines|Y|N|Y|
|Out-of-band \(OOB\) network security|Y|N|N/A|

## ebmg6a, general purpose ECS Bare Metal Instance family

ebmg6a is in invitational preview. To use ebmg6a, [submit a ticket](https://workorder-intl.console.aliyun.com/console.htm).

Features

-   Provides predictable and consistent ultra-high computing, storage, and network performance with the use of the fast path acceleration based on the third-generation X-Dragon architecture.
-   Provides dedicated hardware resources and physical isolation.
-   Equipped with 2.6 GHz AMD EPYC TM ROME processors with a maximum turbo frequency of 3.3 GHz for consistent computing performance.
-   Offers a CPU-to-memory ratio of 1:4.
-   I/O optimized.
-   Supports enhanced SSDs \(ESSDs\), standard SSDs, and ultra disks.
-   Provides ultra-high network performance with a packet forwarding rate of 24,000 Kpps.
-   Supports VPCs only.
-   Suitable for the following scenarios:
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   Third-party virtualization including Xen and KVM, and AnyStack including OpenStack and ZStack
    -   Containers including Docker, Clear Containers, and Pouch
    -   Video encoding, decoding, and rendering
    -   Computing clusters and memory intensive data processing
    -   Data analysis and computing

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|ENIs \(including one primary ENI\)|Disk IOPS \(K\)|Disk bandwidth \(Gbit/s\)|
|:------------|:----|:-------------|:--------------------|--------------------|:------------------------------|:-----------|:---------------------------------|---------------|-------------------------|
|ecs.ebmg6a.64xlarge|256|1024.0|None|64.0|24,000|Yes|31|480|32.0|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmg6e, general purpose ECS Bare Metal Instance family with enhanced performance

Features

-   Provides predictable and consistent ultra-high computing, storage, and network performance with the use of the fast path acceleration based on the third-generation X-Dragon architecture.
-   Provides dedicated hardware resources and physical isolation.
-   I/O optimized.
-   Supports ESSDs.
-   Offers a CPU-to-memory ratio of 1:4.
-   Equipped with 2.5 GHz Intel ® Xeon ® Platinum 8269CY \(Cascade Lake\) processors with a maximum turbo frequency of 3.2 GHz.
-   Provides ultra-high network performance with a packet forwarding rate of 24,000 Kpps.
-   Supports VPCs only.
-   Suitable for the following scenarios:
    -   Scenarios that have high security and regulatory requirements, such as deploying core database services
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   Third-party virtualization including Xen and KVM, and AnyStack including OpenStack and ZStack
    -   Containers including Docker, Clear Containers, and Pouch
    -   Scenarios where large volumes of packets are received and transmitted, such as on-screen video comments and telecom data forwarding
    -   Enterprise-level applications of various types and sizes
    -   Websites and application servers
    -   Game servers
    -   Small and medium-sized database systems, caches, and search clusters
    -   Data analysis and computing
    -   Compute clusters and memory intensive data processing
    -   High-performance scientific and engineering applications

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|Connections \(K\)|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|Disk IOPS \(K\)|Disk bandwidth \(Gbit/s\)|
|:------------|:----|:-------------|:--------------------|:-------------------|:------------------------------|:-----------|-----------------|:---------|:---------------------------------|----------------------------|---------------|-------------------------|
|ecs.ebmg6e.26xlarge|104|384.0|None|30.0|24,000|Yes|1,800|16|31|10|480|20.0|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmg6, general purpose ECS Bare Metal Instance family

Features

-   I/O optimized.
-   Supports ESSDs, standard SSDs, and ultra disks.
-   Offers a CPU-to-memory ratio of 1:3.7.
-   Equipped with 2.5 GHz Intel ® Xeon ® Platinum 8269CY \(Cascade Lake\) processors with a maximum turbo frequency of 3.2 GHz.
-   Provides high network performance with a packet forwarding rate of 6,000 Kpps.
-   Supports VPCs only.
-   Provides dedicated hardware resources and physical isolation.
-   Suitable for the following scenarios:
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   Third-party virtualization including Xen and KVM, and AnyStack including OpenStack and ZStack
    -   Containers including Docker, Clear Containers, and Pouch
    -   Video encoding, decoding, and rendering
    -   Enterprise-level applications such as large and medium-sized databases
    -   Computing clusters and memory intensive data processing
    -   Data analysis and computing

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|
|:------------|:----|:-------------|:--------------------|:-------------------|:------------------------------|:-----------|:---------|:---------------------------------|----------------------------|
|ecs.ebmg6.26xlarge|104|384.0|None|30.0|6,000|Yes|8|32|10|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmc6a, compute optimized ECS Bare Metal Instance family

ebmc6a is in invitational preview. To use ebmc6a, [submit a ticket](https://workorder-intl.console.aliyun.com/console.htm).

Features

-   Provides predictable and consistent ultra-high computing, storage, and network performance with the use of the fast path acceleration based on the third-generation X-Dragon architecture.
-   Provides dedicated hardware resources and physical isolation.
-   Equipped with 2.6 GHz AMD EPYC TM ROME processors with a maximum turbo frequency of 3.3 GHz for consistent computing performance.
-   Offers a CPU-to-memory ratio of 1:2.
-   I/O optimized.
-   Supports ESSDs, standard SSDs, and ultra disks.
-   Provides ultra-high network performance with a packet forwarding rate of 24,000 Kpps.
-   Supports VPCs only.
-   Suitable for the following scenarios:
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   Third-party virtualization including Xen and KVM, and AnyStack including OpenStack and ZStack
    -   Containers including Docker, Clear Containers, and Pouch
    -   Video encoding, decoding, and rendering
    -   Data analysis and computing

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|ENIs \(including one primary ENI\)|Disk IOPS \(K\)|Disk bandwidth \(Gbit/s\)|
|:------------|:----|:-------------|:--------------------|--------------------|:------------------------------|:-----------|:---------------------------------|---------------|-------------------------|
|ecs.ebmc6a.64xlarge|256|512.0|None|64.0|24,000|Yes|31|480|32.0|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmc6e, compute optimized ECS Bare Metal Instance family with enhanced performance

Features

-   Provides predictable and consistent ultra-high computing, storage, and network performance with the use of the fast path acceleration based on the third-generation X-Dragon architecture.
-   Provides dedicated hardware resources and physical isolation.
-   I/O optimized.
-   Supports ESSDs.
-   Offers a CPU-to-memory ratio of 1:2.
-   Equipped with 2.5 GHz Intel ® Xeon ® Platinum 8269CY \(Cascade Lake\) processors with a maximum turbo frequency of 3.2 GHz.
-   Provides ultra-high network performance with a packet forwarding rate of 24,000 Kpps.
-   Supports VPCs only.
-   Suitable for the following scenarios:
    -   Scenarios that have high security and regulatory requirements, such as deploying core database services
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   Third-party virtualization including Xen and KVM, and AnyStack including OpenStack and ZStack
    -   Containers including Docker, Clear Containers, and Pouch
    -   Scenarios where large volumes of packets are received and transmitted, such as on-screen video comments and telecom data forwarding
    -   Web frontend servers
    -   Frontend servers of massively multiplayer online \(MMO\) games
    -   Data analysis, batch processing, and video encoding
    -   High-performance scientific and engineering applications

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|Connections \(K\)|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|Disk IOPS \(K\)|Disk bandwidth \(Gbit/s\)|
|:------------|:----|:-------------|:--------------------|:-------------------|:------------------------------|:-----------|-----------------|:---------|:---------------------------------|----------------------------|---------------|-------------------------|
|ecs.ebmc6e.26xlarge|104|192.0|None|30.0|24,000|Yes|1,800|16|31|10|480|20.0|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmc6, compute optimized ECS Bare Metal Instance family

Features

-   I/O optimized.
-   Supports ESSDs, standard SSDs, and ultra disks.
-   Offers a CPU-to-memory ratio of 1:1.8.
-   Equipped with 2.5 GHz Intel ® Xeon ® Platinum 8269CY \(Cascade Lake\) processors with a maximum turbo frequency of 3.2 GHz.
-   Provides high network performance with a packet forwarding rate of 6,000 Kpps.
-   Supports VPCs only.
-   Provides dedicated hardware resources and physical isolation.
-   Suitable for the following scenarios:
    -   Scenarios where large volumes of packets are received and transmitted, such as on-screen video comments and telecom data forwarding
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   Third-party virtualization including Xen and KVM, and AnyStack including OpenStack and ZStack
    -   Containers including Docker, Clear Containers, and Pouch
    -   Video encoding, decoding, and rendering
    -   Frontend servers of MMO games
    -   High-performance scientific and engineering applications

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|
|:------------|:----|:-------------|:--------------------|:-------------------|:------------------------------|:-----------|:---------|:---------------------------------|----------------------------|
|ecs.ebmc6.26xlarge|104|192.0|None|30.0|6,000|Yes|8|32|10|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmr6a, memory optimized ECS Bare Metal Instance family

ebmr6a is in invitational preview. To use ebmr6a, [submit a ticket](https://workorder-intl.console.aliyun.com/console.htm).

Features

-   Provides predictable and consistent ultra-high computing, storage, and network performance with the use of the fast path acceleration based on the third-generation X-Dragon architecture.
-   Provides dedicated hardware resources and physical isolation.
-   Equipped with 2.6 GHz AMD EPYC TM ROME processors with a maximum turbo frequency of 3.3 GHz for consistent computing performance.
-   Offers a CPU-to-memory ratio of 1:8.
-   I/O optimized.
-   Supports ESSDs, standard SSDs, and ultra disks.
-   Provides ultra-high network performance with a packet forwarding rate of 24,000 Kpps.
-   Supports VPCs only.
-   Suitable for the following scenarios:
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   Third-party virtualization including Xen and KVM, and AnyStack including OpenStack and ZStack
    -   Containers including Docker, Clear Containers, and Pouch
    -   In-memory databases
    -   Data analysis, data mining, and distributed memory caching
    -   Hadoop clusters, Spark clusters, and other memory intensive enterprise applications

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|ENIs \(including one primary ENI\)|Disk IOPS \(K\)|Disk bandwidth \(Gbit/s\)|
|:------------|:----|:-------------|:--------------------|--------------------|:------------------------------|:-----------|:---------------------------------|---------------|-------------------------|
|ecs.ebmr6a.64xlarge|256|2048.0|None|64.0|24,000|Yes|31|480|32.0|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmr6e, memory optimized ECS Bare Metal Instance family with enhanced performance

Features

-   Provides predictable and consistent ultra-high computing, storage, and network performance with the use of the fast path acceleration based on the third-generation X-Dragon architecture.
-   Provides dedicated hardware resources and physical isolation.
-   I/O optimized.
-   Supports ESSDs.
-   Offers a CPU-to-memory ratio of 1:8.
-   Equipped with 2.5 GHz Intel ® Xeon ® Platinum 8269CY \(Cascade Lake\) processors with a maximum turbo frequency of 3.2 GHz.
-   Provides ultra-high network performance with a packet forwarding rate of 24,000 Kpps.
-   Supports VPCs only.
-   Suitable for the following scenarios:
    -   Scenarios that have high security and regulatory requirements, such as deploying core database services
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   Third-party virtualization including Xen and KVM, and AnyStack including OpenStack and ZStack
    -   Containers including Docker, Clear Containers, and Pouch
    -   Scenarios where large volumes of packets are received and transmitted, such as on-screen video comments and telecom data forwarding
    -   High-performance databases and in-memory databases
    -   Data analysis, data mining, and distributed memory caching
    -   Hadoop clusters, Spark clusters, and other memory intensive enterprise applications
    -   High-performance scientific and engineering applications

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|Connections \(K\)|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|Disk IOPS \(K\)|Disk bandwidth \(Gbit/s\)|
|:------------|:----|:-------------|:--------------------|:-------------------|:------------------------------|:-----------|-----------------|:---------|:---------------------------------|----------------------------|---------------|-------------------------|
|ecs.ebmr6e.26xlarge|104|768.0|None|30.0|24,000|Yes|1,800|16|31|10|480|20.0|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmr6, memory optimized ECS Bare Metal Instance family

Features

-   I/O optimized.
-   Supports ESSDs, standard SSDs, and ultra disks.
-   Offers a CPU-to-memory ratio of 1:7.4.
-   Equipped with 2.5 GHz Intel ® Xeon ® Platinum 8269CY \(Cascade Lake\) processors with a maximum turbo frequency of 3.2 GHz.
-   Provides high network performance with a packet forwarding rate of 6,000 Kpps.
-   Supports VPCs only.
-   Provides dedicated hardware resources and physical isolation.
-   Suitable for the following scenarios:
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   Third-party virtualization including Xen and KVM, and AnyStack including OpenStack and ZStack
    -   Containers including Docker, Clear Containers, and Pouch
    -   High-performance databases and in-memory databases
    -   Data analysis, data mining, and distributed memory caching
    -   Hadoop clusters, Spark clusters, and other memory intensive enterprise applications

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|
|:------------|:----|:-------------|:--------------------|:-------------------|:------------------------------|:-----------|:---------|:---------------------------------|----------------------------|
|ecs.ebmr6.26xlarge|104|768.0|None|30.0|6,000|Yes|8|32|10|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmre6p, non-volatile memory optimized ECS Bare Metal Instance family with enhanced performance

To use ebmre6p, [submit a ticket](https://workorder-intl.console.aliyun.com/console.htm).

Features

-   Uses Intel ® Optane TM non-volatile memory.
-   Cost-effective due to end-to-end optimization for ApsaraDB for Redis scenarios.
-   I/O optimized.
-   Supports ESSDs, standard SSDs, and ultra disks.
-   Equipped with 2.5 GHz Intel ® Xeon ® Platinum 8269CY \(Cascade Lake\) processors with a maximum turbo frequency of 3.2 GHz for consistent computing performance.
-   Supports a maximum of 1,920 GiB memory \(384 GiB DRAM memory + 1,536 GiB Intel ® Optane TM non-volatile memory\), offers a CPU-to-memory ratio of about 1:20, and can meet the needs of memory intensive applications.
-   Supports VPCs only.
-   Provides dedicated hardware resources and physical isolation.
-   Suitable for the following scenarios:
    -   In-memory databases such as ApsaraDB for Redis
    -   High-performance databases such as SAP HANA
    -   Other memory intensive applications such as AI applications and smart search applications

Instance types

|Instance type|vCPUs|DRAM \(GiB\)|AEP memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|
|:------------|:----|:-----------|------------------|:--------------------|:-------------------|:------------------------------|:-----------|:---------|:---------------------------------|----------------------------|
|ecs.ebmre6p.26xlarge|104|384.0|1536.0|None|30.0|6,000|Yes|16|31|10|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmre6-6t, memory optimized ECS Bare Metal Instance family with enhanced performance

To use ebmre6-6t, [submit a ticket](https://workorder-intl.console.aliyun.com/console.htm).

Features

-   I/O optimized.
-   Supports ESSDs, standard SSDs, and ultra disks.
-   Offers a CPU-to-memory ratio of 1:30.
-   Equipped with 2.5 GHz Intel ® Xeon ® Platinum 8269 \(Cascade Lake\) processors with a maximum turbo frequency of 3.2 GHz.
-   Provides high network performance with a packet forwarding rate of 6,000 Kpps.
-   Supports VPCs only.
-   Provides dedicated hardware resources and physical isolation.
-   Suitable for the following scenarios:
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   High-performance databases and in-memory databases such as SAP HANA
    -   Memory intensive applications
    -   Big data processing engines such as Apache Spark and Presto

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|
|:------------|:----|:-------------|:--------------------|:-------------------|:------------------------------|:-----------|:---------|:---------------------------------|----------------------------|
|ecs.ebmre6-6t.52xlarge|208|6144.0|None|30.0|6,000|Yes|8|32|10|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmhfg6, general purpose ECS Bare Metal Instance family with high clock speed

Features

-   I/O optimized.
-   Supports ESSDs, standard SSDs, and ultra disks.
-   Offers a CPU-to-memory ratio of 1:4.8.
-   Equipped with 3.1 GHz Intel ® Xeon ® Platinum 8269CY \(Cascade Lake\) processors with a maximum turbo frequency of 3.5 GHz.
-   Provides high network performance with a packet forwarding rate of 6,000 Kpps.
-   Supports VPCs only.
-   Provides dedicated hardware resources and physical isolation.
-   Suitable for the following scenarios:
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   Third-party virtualization including Xen and KVM, and AnyStack including OpenStack and ZStack
    -   Containers including Docker, Clear Containers, and Pouch
    -   Enterprise-level applications such as large and medium-sized databases
    -   Video encoding, decoding, and rendering

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|
|:------------|:----|:-------------|:--------------------|:-------------------|:------------------------------|:-----------|:---------|:---------------------------------|----------------------------|
|ecs.ebmhfg6.20xlarge|80|384.0|None|30.0|6,000|Yes|8|32|10|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmhfc6, compute optimized ECS Bare Metal Instance family with high clock speed

Features

-   I/O optimized.
-   Supports ESSDs, standard SSDs, and ultra disks.
-   Offers a CPU-to-memory ratio of 1:2.4.
-   Equipped with 3.1 GHz Intel ® Xeon ® Platinum 8269CY \(Cascade Lake\) processors with a maximum turbo frequency of 3.5 GHz.
-   Provides high network performance with a packet forwarding rate of 6,000 Kpps.
-   Supports VPCs only.
-   Provides dedicated hardware resources and physical isolation.
-   Suitable for the following scenarios:
    -   Scenarios where large volumes of packets are received and transmitted, such as on-screen video comments and telecom data forwarding
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   Third-party virtualization including Xen and KVM, and AnyStack including OpenStack and ZStack
    -   Containers including Docker, Clear Containers, and Pouch
    -   Video encoding, decoding, and rendering

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|
|:------------|:----|:-------------|:--------------------|:-------------------|:------------------------------|:-----------|:---------|:---------------------------------|----------------------------|
|ecs.ebmhfc6.20xlarge|80|192.0|None|30.0|6,000|Yes|8|32|10|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmhfr6, memory optimized ECS Bare Metal Instance family with high clock speed

Features

-   I/O optimized.
-   Supports ESSDs, standard SSDs, and ultra disks.
-   Offers a CPU-to-memory ratio of 1:9.6.
-   Equipped with 3.1 GHz Intel ® Xeon ® Platinum 8269CY \(Cascade Lake\) processors with a maximum turbo frequency of 3.5 GHz.
-   Provides high network performance with a packet forwarding rate of 6,000 Kpps.
-   Supports VPCs only.
-   Provides dedicated hardware resources and physical isolation.
-   Suitable for the following scenarios:
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   Third-party virtualization including Xen and KVM, and AnyStack including OpenStack and ZStack
    -   Containers including Docker, Clear Containers, and Pouch
    -   High-performance databases and in-memory databases
    -   Data analysis, data mining, and distributed memory caching
    -   Hadoop clusters, Spark clusters, and other memory intensive enterprise applications

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|
|:------------|:----|:-------------|:--------------------|:-------------------|:------------------------------|:-----------|:---------|:---------------------------------|----------------------------|
|ecs.ebmhfr6.20xlarge|80|768.0|None|30.0|6,000|Yes|8|32|10|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmgn6e, GPU-accelerated compute optimized ECS Bare Metal Instance family

ebmgn6e is in invitational preview. To use ebmgn6e, [submit a ticket](https://workorder-intl.console.aliyun.com/console.htm).

Features

-   Provides flexible and powerful software-defined compute based on the X-Dragon architecture.
-   I/O optimized.
-   Supports ESSDs, standard SSDs, and ultra disks.
-   Uses NVIDIA V100 \(32 GB NVLink\) GPU processors.
-   Offers a CPU-to-memory ratio of 1:8.
-   Equipped with 2.5 GHz Intel ® Xeon ® Platinum 8163 \(Skylake\) processors.
-   Uses NVIDIA V100 GPU computing accelerators \(SXM2-based\).
    -   Powered by the new NVIDIA Volta architecture.
    -   Equipped with 32 GB HBM2 GPU memory \(900 GB/s bandwidth\) per GPU.
    -   Equipped with 5,120 CUDA cores per GPU.
    -   Equipped with 640 Tensor cores per GPU.
    -   Supports up to six NVLink connections for a total bandwidth of 300 GB/s \(25 GB/s per connection\).
-   Provides high network performance based on large computing capacity.
-   Suitable for the following scenarios:
    -   Deep learning applications such as training and inference applications of AI algorithms used in image classification, autonomous vehicles, and speech recognition
    -   Scientific computing applications such as computational fluid dynamics, computational finance, molecular dynamics, and environmental analysis

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|GPUs|GPU memory \(GB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|
|:------------|:----|:-------------|:--------------------|----|-----------------|:-------------------|:------------------------------|:-----------|:---------|:---------------------------------|----------------------------|
|ecs.ebmgn6e.24xlarge|96|768.0|None|V100\*8|256|32.0|4,800|Yes|16|8|20|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmgn6v, GPU-accelerated compute optimized ECS Bare Metal Instance family

Features

-   Provides flexible and powerful software-defined compute based on the X-Dragon architecture.
-   I/O optimized.
-   Supports ESSDs, standard SSDs, and ultra disks.
-   Uses NVIDIA V100 GPU processors.
-   Offers a CPU-to-memory ratio of 1:4.
-   Equipped with 2.5 GHz Intel ® Xeon ® Platinum 8163 \(Skylake\) processors.
-   Uses NVIDIA V100 GPU computing accelerators \(SXM2-based\).
    -   Powered by the new NVIDIA Volta architecture.
    -   Equipped with 16 GB HBM2 GPU memory \(900 GB/s bandwidth\) per GPU.
    -   Equipped with 5,120 CUDA cores per GPU.
    -   Equipped with 640 Tensor cores per GPU.
    -   Supports up to six NVLink connections for a total bandwidth of 300 GB/s \(25 GB/s per connection\).
-   Provides high network performance based on large computing capacity.
-   Suitable for the following scenarios:
    -   Deep learning applications such as training and inference applications of AI algorithms used in image classification, autonomous vehicles, and speech recognition
    -   Scientific computing applications such as computational fluid dynamics, computational finance, molecular dynamics, and environmental analysis

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|GPUs|GPU memory \(GB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|
|:------------|:----|:-------------|:--------------------|----|-----------------|:-------------------|:------------------------------|:-----------|:---------|:---------------------------------|----------------------------|
|ecs.ebmgn6v.24xlarge|96|384.0|None|V100\*8|128|30.0|4,500|Yes|8|32|10|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmgn6i, GPU-accelerated compute optimized ECS Bare Metal Instance family

Features

-   Provides flexible and powerful software-defined compute based on the X-Dragon architecture.
-   I/O optimized.
-   Offers a CPU-to-memory ratio of 1:4.
-   Equipped with 2.5 GHz Intel ® Xeon ® Platinum 8163 \(Skylake\) processors.
-   Supports ESSDs that deliver millions of IOPS, standard SSDs, and ultra disks.
-   Uses NVIDIA T4 GPU computing accelerators.
    -   Powered by the new NVIDIA Turing architecture.
    -   Equipped with 16 GB memory \(320 GB/s bandwidth\) per GPU.
    -   Equipped with 2,560 CUDA cores per GPU.
    -   Euipped with up to 320 Turing Tensor cores per GPU.
    -   Mixed-precision Tensor cores support 65 FP16 TFLOPS, 130 INT8 TOPS, and 260 INT4 TOPS.
-   Provides high network performance based on large computing capacity.
-   Suitable for the following scenarios:
    -   AI \(deep learning and machine learning\) inference for computer vision, speech recognition, speech synthesis, natural language processing \(NLP\), machine translation, and recommendation systems
    -   Real-time rendering for cloud gaming
    -   Real-time rendering for AR and VR applications
    -   Graphics workstations or overloaded graphics computing
    -   GPU-accelerated databases
    -   High-performance computing

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|GPUs|GPU memory \(GB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|
|:------------|:----|:-------------|:--------------------|----|-----------------|:-------------------|:------------------------------|:-----------|:---------|:---------------------------------|----------------------------|
|ecs.ebmgn6i.24xlarge|96|384.0|None|T4\*4|64|30.0|4,500|Yes|8|32|10|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmg5s, general purpose ECS Bare Metal Instance family with enhanced network performance

Features

-   I/O optimized.
-   Supports ESSDs, standard SSDs, and ultra disks.
-   Offers a CPU-to-memory ratio of 1:4.
-   Equipped with 2.5 GHz Intel ® Xeon ® Platinum 8163 \(Skylake\) processors with a maximum turbo frequency of 2.7 GHz.
-   Provides high network performance with a packet forwarding rate of 4,500 Kpps.
-   Supports VPCs only.
-   Provides dedicated hardware resources and physical isolation.
-   Suitable for the following scenarios:
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   Third-party virtualization including Xen and KVM, and AnyStack including OpenStack and ZStack
    -   Containers including Docker, Clear Containers, and Pouch
    -   Enterprise-level applications such as large and medium-sized databases
    -   Video encoding

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|
|:------------|:----|:-------------|:--------------------|:-------------------|:------------------------------|:-----------|:---------|:---------------------------------|----------------------------|
|ecs.ebmg5s.24xlarge|96|384.0|None|30.0|4,500|No|8|32|10|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmg5, general purpose ECS Bare Metal Instance family

Features

-   I/O optimized.
-   Supports standard SSDs and ultra disks.
-   Offers a CPU-to-memory ratio of 1:4.
-   Equipped with 2.5 GHz Intel ® Xeon ® Platinum 8163 \(Skylake\) processors with a maximum turbo frequency of 2.7 GHz.
-   Provides high network performance with a packet forwarding rate of 4,000 Kpps.
-   Supports VPCs only.
-   Provides dedicated hardware resources and physical isolation.
-   Suitable for the following scenarios:
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   Third-party virtualization including Xen and KVM, and AnyStack including OpenStack and ZStack
    -   Containers including Docker, Clear Containers, and Pouch
    -   Enterprise-level applications such as large and medium-sized databases
    -   Video encoding

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|
|:------------|:----|:-------------|:--------------------|:-------------------|:------------------------------|:-----------|:---------|:---------------------------------|----------------------------|
|ecs.ebmg5.24xlarge|96|384.0|None|10.0|4,000|No|8|32|10|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmc5s, compute optimized ECS Bare Metal Instance family with enhanced network performance

Features

-   I/O optimized.
-   Supports ESSDs, standard SSDs, and ultra disks.
-   Offers a CPU-to-memory ratio of 1:2.
-   Equipped with 2.5 GHz Intel ® Xeon ® Platinum 8163 \(Skylake\) processors with a maximum turbo frequency of 2.7 GHz.
-   Provides high network performance with a packet forwarding rate of 4,500 Kpps.
-   Supports VPCs only.
-   Provides dedicated hardware resources and physical isolation.
-   Suitable for the following scenarios:
    -   Scenarios where large volumes of packets are received and transmitted, such as on-screen video comments and telecom data forwarding
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   Third-party virtualization including Xen and KVM, and AnyStack including OpenStack and ZStack
    -   Containers including Docker, Clear Containers, and Pouch
    -   Video encoding, decoding, and rendering

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|
|:------------|:----|:-------------|:--------------------|:-------------------|:------------------------------|:-----------|:---------|:---------------------------------|----------------------------|
|ecs.ebmc5s.24xlarge|96|192.0|None|30.0|4,500|No|8|32|10|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmc4, compute optimized ECS Bare Metal Instance family

Features

-   I/O optimized.
-   Supports standard SSDs and ultra disks.
-   Offers a CPU-to-memory ratio of 1:2.
-   Equipped with 2.5 GHz Intel ® Xeon ® E5-2682 v4 \(Broadwell\) processors with a maximum turbo frequency of 2.9 GHz.
-   Provides high network performance with a packet forwarding rate of 4,000 Kpps.
-   Supports VPCs only.
-   Provides dedicated hardware resources and physical isolation.
-   Suitable for the following scenarios:
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   Third-party virtualization including Xen and KVM, and AnyStack including OpenStack and ZStack
    -   Containers including Docker, Clear Containers, and Pouch
    -   Enterprise-level applications such as large and medium-sized databases
    -   Video encoding

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|
|:------------|:----|:-------------|:--------------------|:-------------------|:------------------------------|:-----------|:---------|:---------------------------------|----------------------------|
|ecs.ebmc4.8xlarge|32|64.0|None|10.0|4,000|No|8|12|10|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmr5s, memory optimized ECS Bare Metal Instance family with enhanced network performance

Features

-   I/O optimized.
-   Supports ESSDs, standard SSDs, and ultra disks.
-   Offers a CPU-to-memory ratio of 1:8.
-   Equipped with 2.5 GHz Intel ® Xeon ® Platinum 8163 \(Skylake\) processors with a maximum turbo frequency of 2.7 GHz.
-   Provides high network performance with a packet forwarding rate of 4,500 Kpps.
-   Supports VPCs only.
-   Provides dedicated hardware resources and physical isolation.
-   Suitable for the following scenarios:
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   Third-party virtualization including Xen and KVM, and AnyStack including OpenStack and ZStack
    -   Containers including Docker, Clear Containers, and Pouch
    -   High-performance databases and in-memory databases
    -   Data analysis, data mining, and distributed memory caching
    -   Hadoop clusters, Spark clusters, and other memory intensive enterprise applications

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|
|:------------|:----|:-------------|:--------------------|:-------------------|:------------------------------|:-----------|:---------|:---------------------------------|----------------------------|
|ecs.ebmr5s.24xlarge|96|768.0|None|30.0|4,500|No|8|32|10|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## ebmhfg5, ECS Bare Metal Instance family with high clock speed

Features

-   I/O optimized.
-   Supports standard SSDs and ultra disks.
-   Offers a CPU-to-memory ratio of 1:4.
-   Equipped with 3.7 GHz Intel ® Xeon ® E3-1240v6 \(Skylake\) processors with a maximum turbo frequency of 4.1 GHz.
-   Provides high network performance with a packet forwarding rate of 2,000 Kpps.
-   Supports VPCs only.
-   Provides dedicated hardware resources and physical isolation.
-   Disabled failover by default.

    You can call the [ModifyInstanceMaintenanceAttributes](/intl.en-US/API Reference/Operations and monitoring/ModifyInstanceMaintenanceAttributes.md) operation to modify the maintenance action. Set ActionOnMaintenance to AutoRedeploy to enable failover.

-   Supports Intel ® SGX.
-   Suitable for the following scenarios:
    -   Workloads that require direct access to physical resources or scenarios that require a license to be bound to the hardware
    -   Gaming and finance applications that require high performance
    -   High-performance web servers
    -   Enterprise-level applications such as high-performance databases

Instance types

|Instance type|vCPUs|Memory \(GiB\)|Local storage \(GiB\)|Bandwidth \(Gbit/s\)|Packet forwarding rate \(Kpps\)|IPv6 support|NIC queues|ENIs \(including one primary ENI\)|Private IP addresses per ENI|
|:------------|:----|:-------------|:--------------------|:-------------------|:------------------------------|:-----------|:---------|:---------------------------------|----------------------------|
|ecs.ebmhfg5.2xlarge|8|32.0|None|6.0|2,000|No|8|6|8|

**Note:**

-   You can go to the [ECS Instance Types Available for Each Region page](https://ecs-buy.aliyun.com/instanceTypes/#/instanceTypeByRegion) to view the instance types available in each region.
-   For more information about these specifications, see [Description of instance specifications](/intl.en-US/Instance/Instance families.md).

## Billing methods

ECS Bare Metal Instance supports pay-as-you-go and subscription billing methods. For more information, see [Comparison of billing methods](/intl.en-US/Pricing/Comparison of billing methods.md).

