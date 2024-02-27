# Cloud and virtualization

## Types of cloud

### Public clouds
Cloud-based applications and services offered in a public cloud are made available to the general population. Services may be free or are offered on a pay-per-use model, such as paying for online storage. The public cloud uses the internet to provide services.

### Private clouds
Cloud-based applications and services offered in a private cloud are intended for a specific organization or entity, such as the government. A private cloud can be set up using the private network of an organization, though this can be expensive to build and maintain. A private cloud can also be managed by an outside organization with strict access security.

### Hybrid clouds
A hybrid cloud is made up of two or more clouds (example: part private, part public), where each part remains a separate object, but both are connected using a single architecture. Individuals on a hybrid cloud would be able to have degrees of access to various services based on user access rights.

### Community clouds
A community cloud is created for exclusive use by a specific community. The differences between public clouds and community clouds are the functional needs that have been customized for the community. For example, healthcare organizations must remain compliant with policies and laws (e.g., HIPAA) that require special authentication and confidentiality.

## Virtualization
Virtualization is the foundation of cloud computing. Without it, cloud computing, as it is most-widely implemented, would not be possible.

### Advantages of virtualization
- Less equipment is required. Virtualization enables server consolidation, which requires fewer physical devices and lowers maintenance costs.
- Less energy is consumed. Consolidating servers lowers the monthly power and cooling costs.
- Less space is required. Server consolidation reduces the amount of required floor space.
  
## Hypervisors
The hypervisor is a program, firmware, or hardware that adds an abstraction layer on top of the physical hardware. The abstraction layer is used to create virtual machines which have access to all the hardware of the physical machine such as CPUs, memory, disk controllers, and NICs.

### Types of hypervisors
- type 1
- type 2

### Type 1 hypervisors (bare metal)
- Type 1 hypervisors are also called the “bare metal” approach because the hypervisor is installed directly on the hardware.
- Type 1 hypervisors are usually used on enterprise servers and data center networking devices.

![image](https://github.com/Fong20/Learning-repository/assets/150316121/d0744b3f-19dd-4383-99e7-ecc85ba979d1)

### Type 2 hypervisors (Hosted)
A Type 2 hypervisor is software that creates and runs VM instances. Type 2 hypervisors are also called hosted hypervisors. This is because the hypervisor is installed on top of the existing OS, such as macOS, Windows, or Linux. Then, one or more additional OS instances are installed on top of the hypervisor, as shown in the figure.

![image](https://github.com/Fong20/Learning-repository/assets/150316121/a9cc2576-1c41-4d58-a074-15695bcf9fc9)
