# **RADCraft**
"Rapid Application Deploy Crafting" lets you auto Install or Remove programs from custom package lists.
Feel free to download and modify this simple script with your own Lists (hosting them in a repo) or use the default ones (hosted here in the "Lists" folder).

***NOTE***: Some lists will install programs through APT, some other will install programs with custom commands, the late ones are prone to fail due the complexity of some of this commands, which may include docker, other github repos, etc.

***TIP***: I use the provided lists to make a quick clean deploy of a parrot/kali VM.

------------------------------------------------------------

### **Installation** 

**Install the Script**
```
wget https://raw.githubusercontent.com/M3153N/RADCraft/main/radcraft && chmod +x radcraft && sudo mv radcraft /bin/radcraft
```

**Uninstall**
```
sudo rm -f /bin/radcraft
```



---------------------------------------------------------

### **Usage**

**Install Lists** (you can select multiple lists but *ONLY* **APT** ones)
```
sudo radcraft install <listname1> <listname2>
```
example: **sudo radcraft install common kali**




**Uninstall Lists** (you can select multiple lists but *ONLY* **APT** ones)
```
sudo radcraft remove <listname1> <listname2>
```



**Execute Lists** (you can select multiple lists, but *NEVER* **APT** ones)
```
sudo radcraft execute <listname1> <listname2>
```


-----------------------------------------------------------------------

### **Lists in this Repo**
![Kali](https://raw.githubusercontent.com/ManuMeisen/scripts/main/kali.png)

For **KALI:**

***basic:*** Important hacking software installed through APT.

***extras:*** Some extra software for pentesting, not available to install through APT.

***others:*** Less important hacking software installed through APT.

*Example*: 
```
sudo radcraft install basic && sudo radcraft execute extras
```

```
radcraft execute bins
```
------------------------------------------------------------------
