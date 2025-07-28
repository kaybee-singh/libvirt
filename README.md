# libvirt
In below example we are creating a RHCOS VM. VM name will be testvm and it will have 40 GB of disk.
```bash
git clone https://github.com/kaybee-singh/libvirt/
cd libvirt/xml-files
```
To create a VM with these xml files first create a qcow2 disk for respective VM with below command.
```bash
qemu-img create -f qcow2 /home/karan/vms/testvm.qcow2 40G
Formatting '/home/karan/vms/testvm.qcow2', fmt=qcow2 cluster_size=65536 extended_l2=off compression_type=zlib size=42949672960 lazy_refcounts=off refcount_bits=16

```
Now create the VM
```bash
virsh create rhcos.xml
Domain 'testvm' created from rhcos.xml
```
Now list the create VM
```bash
vrish list --all
```
