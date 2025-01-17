# encoding-checker
A Windows PowerShell script to detect no UTF-8 files.

Fully compatible with CI/CD pipelines on any orchestrator with Windows PowerShell tasks available.


## Parameters

* -path: path to scan. Mandatory.
* -only: If present, determines the file types to check (by extension).
* -exclude: If present, determines the file types to exclude from checking (by extension).
* -showall: If present, shows the full list of scanned files.

## Usage examples

`.\encoding-checker.ps1 -path 'E:\Development\encoding-checker\test files\'`

`.\encoding-checker.ps1 -path 'E:\Development\encoding-checker\test files\' -showall`

`.\encoding-checker.ps1 -path 'E:\Desarrollo\encoding-checker\test files\' -only txt,css,html`

`.\encoding-checker.ps1 -path 'E:\Development\encoding-checker\test files\', 'E:\Another\path\to scan\'`

## CI/CD pipeline example (Azure DevOps)

Configuring the pipeline:

![Script configuration in Azure DevOps pipeline](/img/Pipeline%20config.PNG)

Results:

![Script results in Azure DevOps pipeline](/img/Pipeline%20results.PNG)
