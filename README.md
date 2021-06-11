# ssh2sftp
ssh2sftp   
## Desc
ssh2/sftp go版本   
基于SSH2的安全文件传输协议(SFTP). SFTP不是基于SSH2的FTP协议, 而是一个由IETF SECSH工作组设计的和FTP协议完全没有关系的新协议. SFTP本身不提供认证和安全性, 它依赖下层的SSH2协议提供安全的连接  
**默认允许任意服务器**
## Install
go get https://github.com/zarte/ssh2sftp  
or   
replace github.com/zarte/ssh2sftp => local_path

## Use
### init
ftpClient := Sshsftp.NewFTP() 
### connect
err := ftpClient.Connect(User,Host,Port)
### resume download
err := ftpClient.DownloadResumeFile(remoteFilePath, localLogFilePath)
### scandir
FileInfoList,err := ftpClient.GetList(dir)
### filesize
size,err := ftpClient.size(remoteFilePath)
