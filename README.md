# Openvas

## Objective

This project will be for the set up and configuration of Openvas in a linux environment. Openvas will help aid in vulnerability management and detection.

## Skills Learned


- Proficiency in setting up and configuring Openvas.
- Understanding of launching the GVM services in the command line
- In this demo I learned how to create a task and do a test scan on the machine I'm running for any well known vulnerabilites

## Steps 
- Ran sudo apt-get install openvas
- After install, run gvm-setup
  ![image](https://github.com/Brandencampos/Openvas/assets/62733055/89bce7d5-c9c4-4eef-a03d-f60da171dd52)
- Ran a gvm-check-setup command to check the installation
  ![image](https://github.com/Brandencampos/Openvas/assets/62733055/1e434583-331c-4613-b834-d7ea93e02c90)
- Installtion seems to be ok
  ![image](https://github.com/Brandencampos/Openvas/assets/62733055/bf0003ea-3c93-4cf0-9f72-4a280a7a321b)
- Moved in to the /var/log/gvm directory and opened the gvmd log
  ![image](https://github.com/Brandencampos/Openvas/assets/62733055/6a53a1af-f0b0-4c34-90d8-b1cfda08692f)
- Started a new tab and ran the greenbone-feed-sync --type GVMD_DATA command
  ![image](https://github.com/Brandencampos/Openvas/assets/62733055/c1f25d66-2f04-4bfe-9743-6e5337688f29)
- Running a greenbone-feed-sync --type SCAP command but due to limitations in disk space we won't be able to pull logs and will use this for demeonstration purposes only
  ![image](https://github.com/Brandencampos/Openvas/assets/62733055/99fbcdd7-1090-4247-bd2a-075683854142)
- We'll also be adding the CERT data with the greenbone-feed-sync --type CERT command
  ![image](https://github.com/Brandencampos/Openvas/assets/62733055/e69fc044-3f3d-41ed-81da-68fc4914da73)
- Now we'll start Openvas with the gvm-start command
  ![image](https://github.com/Brandencampos/Openvas/assets/62733055/d923e817-c9c2-4bee-aeeb-21ea304c3573)
- It should then open the web browser and open the page to 127.0.0.1:9392
  ![image](https://github.com/Brandencampos/Openvas/assets/62733055/fd8860d3-fd4b-4641-a7a4-2eab68c44cad)
- You can accept the risk and it will bring you to the log in page
  ![image](https://github.com/Brandencampos/Openvas/assets/62733055/cbd33a25-1849-4f02-b7a1-d276acd08034)
- Once logged in we'll go to the scan section
  ![image](https://github.com/Brandencampos/Openvas/assets/62733055/a6638050-0dcb-4eca-94a7-2843f9b9ce7a)
- We'll click on New Task
![image](https://github.com/Brandencampos/Openvas/assets/62733055/ffb8a36a-d9b8-44ce-bec7-53b09bb102e3)
- We'll name this Test
  ![image](https://github.com/Brandencampos/Openvas/assets/62733055/4e6e0389-0a0a-42a2-ba2a-df5e432ddfa8)
- Click on create a new target
  ![image](https://github.com/Brandencampos/Openvas/assets/62733055/4c97ecd9-d61b-470f-b9c7-cbe0e8451e87)
- Naming this as TEST and for this example we'll be using the ip for the VM
  ![image](https://github.com/Brandencampos/Openvas/assets/62733055/c42f252e-27dc-4ec4-9081-c3eab240ea31)
- After saving we'll come back to the test task and hit save
  ![image](https://github.com/Brandencampos/Openvas/assets/62733055/53e08b23-97bb-4b0a-804e-1c721c6070ab)
- And now the task will be there for the scan
  ![image](https://github.com/Brandencampos/Openvas/assets/62733055/7368579b-1019-4c2e-b9b0-f73c030ac8f7)
- After a few minutes we'll see the scan has completed and there is a report to view
  ![image](https://github.com/Brandencampos/Openvas/assets/62733055/8a6d802e-2b44-416b-9fa5-55fcb57f05d4)










