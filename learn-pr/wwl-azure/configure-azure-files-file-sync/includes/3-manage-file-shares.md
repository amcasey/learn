
To use Azure Files, you need an Azure storage account. After you have a storage account, you can create and configure a file share by using Azure Files in the Azure portal.

:::image type="content" source="../media/create-file-shares-bf2e2f1d.png" alt-text="Screenshot that shows how to configure a new SMB Azure file share using the Azure portal.":::

### Considerations for using SMB Azure file shares

There are two important settings that you need to be aware of when creating and configuring SMB Azure file shares.

- **Open port 445**. Azure Files uses the SMB protocol. SMB communicates over TCP port 445. Be sure port 445 is open. Also, make sure your firewall isn't blocking TCP port 445 from the client machine.

- **Enable secure transfer**. The `Secure transfer required` setting enhances the security of your storage account by limiting requests to your storage account from secure connections only. Consider the scenario where you use REST APIs to access your storage account. If you attempt to connect, and secure transfer required is enabled, you must connect by using HTTPS. If you try to connect to your account by using HTTP, and secure transfer required is enabled, the connection is rejected.

## Map SMB Azure file share on Windows

You can connect to your Azure file share with Windows or Windows Server in the Azure portal. Specify the **Drive** where you want to map the share, and choose the **Authentication method**. The system supplies you with PowerShell commands to run when you're ready to work with the file share. This video shows how to mount an Azure file share in Windows.  

> [!VIDEO https://www.youtube.com/embed/bmRZi9iGsK0]

## Mount SMB Azure file share on Linux

You can also connect to Azure file shares from Linux machines. From your virtual machine page, select **Connect**. SMB Azure file shares can be mounted in Linux distributions by using the CIFS kernel client. File mounting can be done on-demand with the `mount` command or on-boot (persistent) by creating an entry in /etc/fstab.

:::image type="content" source="../media/map-file-shares-linux-1639a49a.png" alt-text="Screenshot that shows how to connect to an Azure file share with Linux in the Azure portal.":::
