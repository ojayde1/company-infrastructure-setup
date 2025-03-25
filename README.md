# company-infrastructure-setup

This repository contains the steps and commands used to set up the server infrastructure for a small business. It includes user creation, group assignments, and setting up company directories with appropriate permissions.

## Users and Groups

### Users:
- Andrew, System Administrator
- Julius, Legal
- Chizi, Human Resource Manager
- Jeniffer, Sales Manager
- Adeola, Business Strategist
- Bach, CEO
- Gozie, IT Intern
- Ogochukwu, Finance Manager

### Company Directories:
- Finance Budgets
- Contract Documents
- Business Projections
- Business Models
- Employee Data
- Company Vision and Mission Statement
- Server Configuration Script

## Steps

### 1. Create Users:
Each user was created using the `adduser` command:

sudo adduser andrew
sudo adduser julius
sudo adduser chizi
sudo adduser jeniffer
sudo adduser adeola
sudo adduser bach
sudo adduser gozie
sudo adduser ogochukwu

### 2. Create Groups:
Each group was created using the `addgroup` command:
sudo groupadd sysadmin
sudo groupadd legal
sudo groupadd hr
sudo groupadd sales
sudo groupadd strategy
sudo groupadd executives
sudo groupadd intern
sudo groupadd finance

### 3. Assigning users to Groups:
Each user was assigned to a group using the `usermod` command:

sudo usermod -aG sysadmin andrew
sudo usermod -aG legal julius
sudo usermod -aG hr chizi
sudo usermod -aG sales jeniffer
sudo usermod -aG strategy adeola
sudo usermod -aG executives bach
sudo usermod -aG intern gozie
sudo usermod -aG finance ogochukwu

### 4. Created Company Directories:
Each directory  was created using the `mkdir` command under /company/:

sudo mkdir -p /company/finance_budgets
sudo mkdir -p /company/contract_documents
sudo mkdir -p /company/business_projections
sudo mkdir -p /company/business_models
sudo mkdir -p /company/employee_data
sudo mkdir -p /company/vision_mission
sudo mkdir -p /company/server_configs

### 4. Set Ownership and Permissions Directories:
Each directory was assigned ownership and access permissions using the `chown` and `chmod` commands:

sudo chown -R ogochukwu:finance /company/finance_budgets
sudo chmod -R 770 /company/finance_budgets

sudo chown -R julius:legal /company/contract_documents
sudo chmod -R 770 /company/contract_documents

sudo chown -R chizi:hr /company/employee_data
sudo chmod -R 770 /company/employee_data

sudo chown -R jeniffer:sales /company/business_models
sudo chmod -R 770 /company/business_models

sudo chown -R adeola:strategy /company/business_projections
sudo chmod -R 770 /company/business_projections

sudo chown -R bach:executives /company/vision_mission
sudo chmod -R 770 /company/vision_mission

sudo chown -R andrew:sysadmin /company/server_configs
sudo chmod -R 770 /company/server_configs






