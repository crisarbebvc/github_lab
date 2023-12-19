### Features

- Extract changed files with yumemi-inc/changed-files@v3
- File transfer FTP with kevinpainchaud/simple-ftp-deploy-action@v1.2.1

# GitHub Actions for transferring BackOffice Components

![](https://www.valoraanalitik.com/wp-content/uploads/2023/11/bvc-bolsa-de-valores-de-colombia-696x406.jpg)


**Table of Contents**

[TOCM]

[TOC]

#Two Important components in Actions

###Extract name of files to transfer in specific folder in Tandem Server

> Servers (SR*), Dictionaries (DI*) and Forms (FM*)

####Code Block

Example for Servers:

    with: 
         patterns: |
              **/SR*
    

###Transfer Files to Tandem Server

> Servers (SR*) in tandem/SRC, Dictionaries (DI*) in tandem/DIC and Forms (FM*) in tandem/LBR

###FlowChart

```flow
st=>start: push to main branch
op=>operation: Workflow start
op2=>operation: Get Latest Code
op3=>operation: Changed Files
cond=>condition: Are there modified files?
op4=>operation: Transfer Files
e=>end: End Workflow

st->op->op2->op3->cond
cond(yes)->op4->e
cond(no)->e
```

###Sequence Diagram for Server Components
                    
```seq
changed_src->put_src: Changed Files 
Note right of put_src: Transfer\nFiles
changed_src->end: No Changed Files 
put_src-->changed_src: Other Component File
```