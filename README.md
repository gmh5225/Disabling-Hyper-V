# Disabling-Hyper-V

Certain advanced Windows 10 features, such as _Device Guard_ (in particular,
_Hypervisor-protected code integrity_ or HVCI) and _Credential Guard_, can
prevent Hyper-V from being completely disabled. In other words, when any of
these features are enabled, so is Hyper-V, even though Windows may report
otherwise.

The _Device Guard and Credential Guard hardware readiness tool_ released by
Microsoft can disable the said Windows 10 features along with Hyper-V:
1. Download the latest version of the tool from [here](https://www.microsoft.com/en-us/download/details.aspx?id=53337) dgreadiness-tool. The
following steps assume version 3.6.
1. Unzip.
1. Open an **elevated** (i.e. _Run as administrator_) Command Prompt.
1. `@powershell -ExecutionPolicy RemoteSigned -Command "X:\path\to\dgreadiness_v3.6\DG_Readiness_Tool_v3.6.ps1 -Disable"`
1. Reboot.
