# Prework_Setup_Laptop

# Aplicaciones.

Nota: Para poder vizualizar las aplicaciones instaladas utilize los siguientes comandos.

    Get-WmiObject -Class Win32_Product | Select-Object -Property Name | Out-File -FilePath aplicaciones.txt

# Caracteristicas.

Nota: Para poder vizualizar caracteristicas instaladas utilize los siguientes comandos.

    Get-WmiObject -Class Win32_Product | Select-Object -Property Name | Out-File -FilePath aplicaciones.txt
    Get-WindowsOptionalFeature -Online | Select-Object -Property FeatureName | Out-File -FilePath caracteristicas.txt

# Programas.

Nota: Para poder vizualizar las extensiones instaladas utilize los siguientes comandos.

    Get-ItemProperty HKLM:\Software\Wow6432Node\Microsoft\Windows\CurrentVersion\Uninstall\* | Select-Object DisplayName, DisplayVersion, Publisher, InstallDate | Format-Table –AutoSize > D:\Prework_Setup_Laptop\Programas\programas.txt

# Extensiones: Visual Studio Code.

Nota: Para poder vizualizar las extensiones instaladas utilize los siguientes comandos.

    code --list-extensions
    code --list-extensions > extensiones.txt
