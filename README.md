# **Meisen**
Auto Install or Remove programs from custom package lists.
Feel free to download and modify this simple script with your own Lists (hosting them in a repo) or use the default ones (hosted here in the "Lists" folder).

***NOTE***: Some lists will install programs through APT, some other will install programs with custom commands, the late ones are prone to fail due the complexity of some of this commands, which may include docker, other github repos, etc.

***TIP***: If you want to work with the default lists provided here, i recommend to install the package list *common* first, as it installs many of the base software and requirement packages for more complex software.

------------------------------------------------------------

### **Installation** 

**Python script from this repo:**
```
wget https://raw.githubusercontent.com/ManuMeisen/Meisen/main/meisen && chmod +x meisen && sudo mv meisen /bin/meisen
```

**Lastest binary from releases:**
```
wget https://github.com/ManuMeisen/Meisen/releases/latest/download/meisen_amd64_linux && chmod +x meisen_amd64_linux && sudo mv meisen_amd64_linux /bin/meisen
```

**Uninstall**
```
sudo rm -f /bin/meisen
```



---------------------------------------------------------

### **Usage**

**Install Lists** (you can select multiple lists but *ONLY* **APT** ones)
```
sudo meisen install <listname1> <listname2>
```
example: **sudo meisen install common kali**




**Uninstall Lists** (you can select multiple lists but *ONLY* **APT** ones)
```
sudo meisen remove <listname1> <listname2>
```
example: **sudo meisen remove home kali**



**Execute Lists** (you can select multiple lists, but *NEVER* **APT** ones)
```
sudo meisen execute <listname1> <listname2>
```
example: **sudo meisen execute parrot extras**


-----------------------------------------------------------------------

### **Lists in this Repo**

For **BOTH KALI & PARROT:**
-***common:*** Essential  software for any serious pentesting/hacking Distro (Install this **FIRST**).
-***extras:*** Some extra software for pentesting, not available to install through APT.

For **PARROT OS:**  
-***home:*** Basic software that comes in the *home* edition of Parrot os. (I usually remove this one to unbloat my VM)
-***parrot:*** Important hacking software that cannot be installed through APT.

For **KALI LINUX:**
-***kali:*** the equivalent of the *parrot* list but installable through APT.



