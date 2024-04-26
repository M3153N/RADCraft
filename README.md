# **Meisen**
Auto Install or Remove programs from custom package lists.
Feel free to download and modify this simple script with your own Lists (hosting them in a repo) or use the default ones (hosted here in the "Lists" folder).

***NOTE***: Some lists will install programs through APT, some other will install programs with custom commands, the late ones are prone to fail due the complexity of some of this commands, which may include docker, other github repos, etc.

***TIP***: I use the provided lists to make a quick clean deploy of a parrot/kali VM.

------------------------------------------------------------

### **Installation Options** 

**Lastest binary from releases**   <------*Recommended*
```
wget https://github.com/ManuMeisen/Meisen/releases/latest/download/meisen_amd64_linux && chmod +x meisen_amd64_linux && sudo mv meisen_amd64_linux /bin/meisen
```

**Python script from this repo**
```
wget https://raw.githubusercontent.com/ManuMeisen/Meisen/main/meisen && chmod +x meisen && sudo mv meisen /bin/meisen
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
![Kali](https://raw.githubusercontent.com/ManuMeisen/scripts/main/parrot.png)

For **PARROT OS:**  

***home:*** Basic software that comes in the *home* edition of Parrot OS. (I usually remove this one to unbloat my VM)

***parrot:*** Important hacking software installed through APT.

***parrotext:*** Some extra software for pentesting, not available to install through APT, plus some configs.

*Example*: 
```
sudo meisen remove home && sudo meisen install parrot && sudo meisen execute parrotext
```

![Kali](https://raw.githubusercontent.com/ManuMeisen/scripts/main/kali.png)

For **KALI LINUX:**

***kali:*** Important hacking software installed through APT.

***kaliext:*** Some extra software for pentesting, not available to install through APT, plus some configs.

*Example*: 
```
sudo meisen install kali && sudo meisen execute kaliext
```


**OTHER**:

***binaries:*** Standalone binaries for Windows and Linux, plus some Shell scripts. *TIP*: dont use sudo when selecting this list.

*Example*: 
```
meisen execute binaries
```


------------------------------------------------------------------
