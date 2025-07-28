# libvirt
In below example we are creating a RHCOS VM. VM name will be testvm and it will have 40 GB of disk.
```bash
git clone https://github.com/kaybee-singh/libvirt/
cd libvirt/xml-files
```
To create a VM with these xml files first create a qcow2 disk for respective VM with below command.
```bash
qemu-img create -f qcow2 testvm.qcow2 40G
```
Now create the VM
```bash
virsh create rhcos.xml
```
Now list the create VM
```bash
vrish list --all
```
