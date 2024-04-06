# **Meisen**
Auto Install/Remove/Execute programs and commands from GitHub Repo's Lists.

### **Installation** 
```
sudo wget https://github.com/ManuMeisen/Meisen/blob/main/meisen && chmod +x meisen && sudo mv meisen /bin/kerbrute
```
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



**Exec Lists** (you can select multiple lists, but *NEVER* **APT** ones)
```
sudo meisen exec <listname1> <listname2>
```
example: **sudo meisen exec parrot extras**



### **Lists in this Repo**
For **PARROT OS:**
*home:*
*parrot:*

For **KALI LINUX:**
*kali:*

For **BOTH KALI & PARROT:**
*common:*
*extras:*

