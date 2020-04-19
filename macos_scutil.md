# Using the "scutil" tool in MacOS systems

## Change Host Name
```bash
sudo scutil --set HostName <name>
sudo scutil --set LocalHostName <name>
sudo scutil --set ComputerName <name>
dscacheutil -flushcache
```
