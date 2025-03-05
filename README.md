![image](https://github.com/user-attachments/assets/48be44fd-386e-462c-92f2-9cf517d4779c)

I set up a cloud storage system similar to AWS S3 and uploaded the raw data. Then, I configured a VM with the necessary access permissions, which provided an SSH-in-browser feature to install Python and run Mage. Due to multiple IP addresses, I won't be sharing screenshots.
On the VM, I installed Python, pip, and Mage, then started a project. I added a block to import data and a transformer block that follows the Jupyter Notebook in my repo. However, whenever I ran the transformer block that processes eight datasets into tables, the kernel restarted and never recovered. Restarting Mage through the terminal resulted in the same issue.
It turned out that Mage was bugging out when converting eight datasets into dictionaries. Instead, returning them as a tuple of dataframes fixed the issue.

Then I created a user and credentials so I can connect to big query and push data to it. The final mage pipeline looks like this:

![mage_pipeline](https://github.com/user-attachments/assets/f655899e-aac8-4466-b906-a65e9ade8f60)

![image](https://github.com/user-attachments/assets/9bedc2d2-9ddc-445a-9f03-9cbd2c25aa0d)

This took a bit of debugging as well due to uninstalled packages and putting access keys and secrets i n the right place and format.

![image](https://github.com/user-attachments/assets/18626d61-e75b-4118-8389-3c3fb2d8d497)

So for the final step ~ using looker for some kind of a visualisation dashboard:

![image](https://github.com/user-attachments/assets/dcdbe2c8-6aad-4b3b-b035-9efef7810244)




