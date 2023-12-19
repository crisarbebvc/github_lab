### Features

- Extract changed files with yumemi-inc/changed-files@v3
- File transfer FTP with kevinpainchaud/simple-ftp-deploy-action@v1.2.1

# GitHub Actions for transferring BackOffice Components

![](https://www.valoraanalitik.com/wp-content/uploads/2023/11/bvc-bolsa-de-valores-de-colombia-696x406.jpg)


Two Important components in Actions

Extract name of files to transfer in specific folder in Tandem Server

> Servers (SR*), Dictionaries (DI*) and Forms (FM*)

Code Block

Example for Servers:

    with: 
         patterns: |
              **/SR*
    

Transfer Files to Tandem Server

> Servers (SR*) in tandem/SRC, Dictionaries (DI*) in tandem/DIC and Forms (FM*) in tandem/LBR