# email
邮箱验证
 
 邮件发送类
* 支持发送纯文本邮件和HTML格式的邮件，可以多收件人，多抄送，多秘密抄送，带附件(单个或多个附件),支持到服务器的ssl连接
* 需要的php扩展：sockets、Fileinfo和openssl。
* 编码格式是UTF-8，传输编码格式是base64
* @example
* $mail = new MySendMail();
* $mail->setServer("smtp@126.com", "XXXXX@126.com", "XXXXX"); //设置smtp服务器，普通连接方式
* $mail->setServer("smtp.gmail.com", "XXXXX@gmail.com", "XXXXX", 465, true); //设置smtp服务器，到服务器的SSL连接
* $mail->setFrom("XXXXX"); //设置发件人
* $mail->setReceiver("XXXXX"); //设置收件人，多个收件人，调用多次
* $mail->setCc("XXXX"); //设置抄送，多个抄送，调用多次
* $mail->setBcc("XXXXX"); //设置秘密抄送，多个秘密抄送，调用多次
* $mail->addAttachment( array("XXXX","xxxxx") ); //添加附件，多个附件，可调用多次，第一个文件名是 程序要去抓的文件名，第二个文件名是显示在邮件中的文件名。
* $mail->setMail("test", "<b>test</b>"); //设置邮件主题、内容
* $mail->sendMail(); //发送
